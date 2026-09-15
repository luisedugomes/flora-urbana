# 🛠️ Especificação Técnica (Tech Spec) - Flora Urbana

Este documento detalha a arquitetura técnica, o modelo de dados e os contratos de API (via JSON Server) necessários para o funcionamento do e-commerce **Flora Urbana**.

A aplicação utiliza uma arquitetura frontend baseada em **HTML, CSS e JavaScript**, com consumo de uma **API Fake implementada através do JSON Server** para disponibilização dos produtos e armazenamento das informações relacionadas aos pedidos.

---

## 1. Modelo de Dados (Diagrama ER)

Abaixo está o Diagrama Entidade-Relacionamento (DER) que representa a estrutura do banco de dados simulado (`db.json`) e como as informações se relacionam.

```mermaid
erDiagram
    CLIENTE ||--o{ PEDIDO : "realiza"
    PEDIDO ||--|{ ITEM_PEDIDO : "possui"
    PRODUTO ||--o{ ITEM_PEDIDO : "compõe"
    
    CLIENTE {
        string id PK "Gerado automaticamente"
        string nome
        string email
        string telefone
    }

    PRODUTO {
        string id PK "Gerado automaticamente"
        string nome
        string categoria
        float preco
        string descricao
        string imagem
        int estoque
    }

    PEDIDO {
        string id PK
        string clienteId FK "Vínculo com o Cliente"
        string data
        float subtotal
        float frete
        float total
        string status
        string formaPagamento
        string formaEntrega
        string endereco
    }

    ITEM_PEDIDO {
        string id PK
        string pedidoId FK "Vínculo com o Pedido"
        string produtoId FK "Vínculo com o Produto"
        int quantidade
        float precoUnitario
        float subtotal
    }
```

### Relacionamentos

* Um **Cliente** pode realizar vários **Pedidos**.
* Cada **Pedido** pertence a um único **Cliente**.
* Um **Pedido** possui um ou mais **Itens de Pedido**.
* Cada **Item de Pedido** está relacionado a um único **Produto**.
* Um **Produto** pode aparecer em vários **Itens de Pedido**.
* O preço utilizado no item é armazenado no momento da compra para manter o histórico do pedido.

---

## 2. Dicionário de Dados

Breve explicação das principais entidades utilizadas pela aplicação.

### 🌱 Produtos

Responsável por armazenar as informações dos produtos comercializados pela Flora Urbana.

* **id:** Identificador único do produto, gerado pelo JSON Server.
* **nome:** Nome comercial da planta ou produto.
* **categoria:** Categoria à qual o produto pertence, como "Plantas", "Vasos", "Acessórios" ou "Jardinagem".
* **preco:** Valor de venda do produto, armazenado como número decimal (Float).
* **descricao:** Descrição e informações relevantes sobre o produto.
* **imagem:** Caminho ou URL da imagem utilizada na apresentação do produto.
* **estoque:** Quantidade disponível do produto para venda.

### 👤 Clientes

Responsável por armazenar os dados básicos dos clientes que realizam pedidos.

* **id:** Identificador único do cliente.
* **nome:** Nome completo do cliente.
* **email:** Endereço de e-mail utilizado para contato.
* **telefone:** Número de telefone do cliente.

### 🛒 Pedidos

Responsável por registrar as compras realizadas pelos clientes.

* **id:** Identificador único do pedido.
* **clienteId:** Chave estrangeira que relaciona o pedido ao cliente responsável pela compra.
* **data:** Data de criação do pedido no formato ISO (`YYYY-MM-DD`).
* **subtotal:** Soma dos valores dos produtos antes do frete.
* **frete:** Valor cobrado pela entrega.
* **total:** Valor final do pedido, considerando subtotal e frete.
* **status:** Situação atual do pedido, como "PENDENTE", "CONFIRMADO" ou "CANCELADO".
* **formaPagamento:** Método de pagamento selecionado pelo cliente.
* **formaEntrega:** Método de entrega escolhido pelo cliente.
* **endereco:** Endereço utilizado para entrega do pedido.

### 📦 Itens do Pedido

Responsável por registrar individualmente cada produto presente em um pedido.

* **id:** Identificador único do item.
* **pedidoId:** Chave estrangeira que relaciona o item ao pedido.
* **produtoId:** Chave estrangeira que identifica o produto comprado.
* **quantidade:** Quantidade do produto adicionada ao pedido.
* **precoUnitario:** Preço do produto no momento da compra.
* **subtotal:** Resultado da multiplicação do preço unitário pela quantidade.

### ⚠️ Regra de Negócio Crítica

A quantidade solicitada pelo cliente **não pode ultrapassar o estoque disponível**.

O cálculo de cada item deve seguir a fórmula:

```text
subtotal = precoUnitario × quantidade
```

O valor final do pedido deve seguir:

```text
total = subtotal + frete
```

---

## 3. Rotas da API (JSON Server)

A aplicação consome uma API local simulada pelo JSON Server. Abaixo estão os principais endpoints utilizados pelo sistema.

### 🌱 Produtos

* `GET /produtos` — Retorna todos os produtos disponíveis.
* `GET /produtos/:id` — Retorna os dados de um produto específico.
* `POST /produtos` — Cadastra um novo produto.
* `PUT /produtos/:id` — Atualiza os dados de um produto.
* `DELETE /produtos/:id` — Remove um produto.

### 👤 Clientes

* `GET /clientes` — Retorna a lista de clientes.
* `GET /clientes/:id` — Retorna um cliente específico.
* `POST /clientes` — Cadastra um novo cliente.
* `PUT /clientes/:id` — Atualiza os dados de um cliente.

### 🛒 Pedidos

* `GET /pedidos` — Retorna todos os pedidos cadastrados.
* `GET /pedidos/:id` — Retorna um pedido específico.
* `GET /pedidos?clienteId=1` — Retorna os pedidos de um cliente específico.
* `POST /pedidos` — Registra um novo pedido.
* `PUT /pedidos/:id` — Atualiza um pedido.
* `DELETE /pedidos/:id` — Remove um pedido.

### 📦 Itens do Pedido

* `GET /itensPedido` — Retorna todos os itens dos pedidos.
* `GET /itensPedido?pedidoId=1` — Retorna os itens pertencentes a um pedido específico.
* `POST /itensPedido` — Cadastra um novo item de pedido.
* `PUT /itensPedido/:id` — Atualiza um item.
* `DELETE /itensPedido/:id` — Remove um item.

---

## 4. Estrutura do Banco de Dados (db.json)

Esta é a representação em formato JSON do banco de dados simulado.

A estrutura serve de contexto para ferramentas de IA e para o **JSON Server** inicializar a API Fake.

```json
{
  "clientes": [
    {
      "id": "1",
      "nome": "Maria Silva",
      "email": "maria@email.com",
      "telefone": "(42) 99999-9999"
    }
  ],

  "produtos": [
    {
      "id": "1",
      "nome": "Costela-de-Adão",
      "categoria": "Plantas",
      "preco": 89.90,
      "descricao": "Planta ornamental ideal para ambientes internos.",
      "imagem": "img/produtos/costela-de-adao.jpg",
      "estoque": 10
    },
    {
      "id": "2",
      "nome": "Jiboia",
      "categoria": "Plantas",
      "preco": 49.90,
      "descricao": "Planta de fácil cultivo e ótima para ambientes internos.",
      "imagem": "img/produtos/jiboia.jpg",
      "estoque": 15
    },
    {
      "id": "3",
      "nome": "Vaso de Cerâmica",
      "categoria": "Vasos",
      "preco": 59.90,
      "descricao": "Vaso de cerâmica para decoração e cultivo de plantas.",
      "imagem": "img/produtos/vaso-ceramica.jpg",
      "estoque": 8
    }
  ],

  "pedidos": [
    {
      "id": "1",
      "clienteId": "1",
      "data": "2026-09-13",
      "subtotal": 139.80,
      "frete": 15.00,
      "total": 154.80,
      "status": "CONFIRMADO",
      "formaPagamento": "PIX",
      "formaEntrega": "ENTREGA_PADRAO",
      "endereco": "Rua das Flores, 100 - Centro"
    }
  ],

  "itensPedido": [
    {
      "id": "1",
      "pedidoId": "1",
      "produtoId": "1",
      "quantidade": 1,
      "precoUnitario": 89.90,
      "subtotal": 89.90
    },
    {
      "id": "2",
      "pedidoId": "1",
      "produtoId": "2",
      "quantidade": 1,
      "precoUnitario": 49.90,
      "subtotal": 49.90
    }
  ]
}
```
## 4. Técnologias

Técnologias que serão utilizadas:

* **Bootstrap v5.3.3:** Framework css.
* * **ViaCEp:** Api utilizada para encontrar o código de endereço postal desejado. ( Não possui indentificação de versionamento para o público).
