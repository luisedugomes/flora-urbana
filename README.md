# 🌿 flora-urbana

### **Autor:** Luis Eduardo Gomes

A **Flora Urbana** é uma aplicação web de e-commerce desenvolvida para uma loja virtual especializada na comercialização de plantas, vasos e produtos relacionados à jardinagem.

O projeto tem como objetivo proporcionar uma experiência de compra simples, intuitiva e responsiva, permitindo que os usuários naveguem pelo catálogo de produtos, consultem informações, adicionem itens ao carrinho e realizem o preenchimento de dados necessários para a compra.

O frontend da aplicação foi desenvolvido utilizando **HTML, CSS e JavaScript**, com o apoio de um **Framework CSS** para criação de layouts responsivos e componentes visuais. O backend é simulado por meio de uma **API Fake utilizando JSON Server**, responsável pelo armazenamento e disponibilização dos dados dos produtos e demais informações utilizadas pela aplicação.

---

## 📚 Documentação do Projeto

Para compreender as regras de negócio, o escopo e a arquitetura técnica da aplicação, consulte os documentos abaixo:

* [📄 Product Requirements Document (PRD)](docs/prd.md) — Visão geral do projeto, público-alvo, funcionalidades, atores e histórias de usuário.
* [🛠️ Especificação Técnica (Tech Spec)](docs/spec.md) — Arquitetura da aplicação, estrutura de dados, diagrama de banco de dados (DER), dicionário de dados e rotas da API.
* [🎨 Design System](docs/design-system.md) — Definição da identidade visual, cores, tipografia e padrões dos componentes utilizados na aplicação.

---

## 🎨 Design

A identidade visual da **Flora Urbana** foi desenvolvida com foco em uma estética natural, moderna e agradável, buscando transmitir os conceitos de natureza, sustentabilidade e bem-estar.

Principais características:

* 🌱 Paleta de cores inspirada na natureza;
* 🌿 Elementos visuais relacionados a plantas e jardinagem;
* 📱 Layout responsivo para dispositivos móveis e desktop;
* 🛒 Interface voltada para experiência de compra;
* 🖼️ Cards para apresentação dos produtos;
* 🔎 Organização intuitiva do catálogo;
* ✨ Design consistente entre todas as páginas.

### Protótipo

* [🖼️ Protótipo no Figma](#) — Telas interativas da aplicação.

---

## 🌐 Site em Produção

A aplicação poderá ser disponibilizada utilizando **GitHub Pages** ou outra plataforma de hospedagem compatível com projetos frontend.

🔗 **Site:** [Flora Urbana](#)

---

## 💻 Tecnologias e Dependências

### Frontend

* **HTML5** — Estruturação das páginas da aplicação.
* **CSS3** — Estilização e personalização dos componentes.
* **JavaScript** — Lógica da aplicação, manipulação do DOM e interatividade.
* **Framework CSS** — Utilizado para criação de componentes e layouts responsivos.
* **jQuery** — Manipulação do DOM, eventos e interações da interface.

### Backend / API

* **JSON Server** — Utilizado para simular uma API REST e disponibilizar os dados da aplicação.

### Ferramentas

* **Node.js** — Ambiente de execução para ferramentas JavaScript.
* **NPM** — Gerenciamento de dependências.
* **Git** — Controle de versão.
* **GitHub** — Hospedagem do código-fonte e gerenciamento do projeto.
* **Visual Studio Code** — Editor utilizado durante o desenvolvimento.

---

# 🛒 Principais Funcionalidades

A aplicação **Flora Urbana** possui como objetivo disponibilizar as principais funcionalidades de um e-commerce:

* 🏠 Página inicial com apresentação da loja;
* 🌱 Catálogo de plantas e produtos;
* 🔎 Busca e filtragem de produtos;
* 🪴 Visualização dos detalhes de cada produto;
* 🛒 Adição e remoção de produtos do carrinho;
* 💰 Cálculo do subtotal e valor total da compra;
* 👤 Cadastro/preenchimento de dados do cliente;
* 📍 Cadastro de endereço para entrega;
* 📦 Seleção de opções relacionadas à entrega;
* 💳 Simulação do processo de checkout;
* ✅ Validação dos formulários;
* 🔄 Comunicação com API Fake utilizando requisições assíncronas.

---

# 🗂️ Estrutura do Projeto

```text
flora-urbana/
│
├── docs/
│   ├── prd.md
│   ├── spec.md
│   └── design-system.md
│
├── css/
│   ├── style.css
│   └── ...
│
├── js/
│   ├── main.js
│   ├── produtos.js
│   ├── carrinho.js
│   └── ...
│
├── img/
│   ├── produtos/
│   ├── banners/
│   └── ...
│
├── index.html
├── produtos.html
├── produto.html
├── carrinho.html
├── checkout.html
├── db.json
├── routes.json
├── package.json
├── .gitignore
└── README.md
```

---

# ✅ Checklist | Indicadores de Desempenho (ID) dos Resultados de Aprendizagem (RA)

## RA1 - Utilizar Frameworks CSS para estilização de elementos HTML e criação de layouts responsivos.

* [ ] **ID 01** - Prototipa interfaces adaptáveis para no mínimo os tamanhos de tela mobile e desktop, utilizando ferramentas de design como Figma ou ferramentas de IA.
* [ ] **ID 02** - Implementa layout responsivo utilizando Framework CSS, como Bootstrap, Materialize, Tailwind + DaisyUI, utilizando Flexbox ou Grid.
* [ ] **ID 03** - Implementa layout responsivo com CSS puro, utilizando Flexbox ou Grid Layout.
* [ ] **ID 04** - Utiliza componentes prontos de um Framework CSS, como cards, botões, navbar, formulários e componentes JavaScript.
* [ ] **ID 05** - Cria layouts fluidos utilizando unidades relativas como `%`, `rem`, `em`, `vw` e `vh`.
* [ ] **ID 06** - Aplica um Design System consistente, contemplando cores, tipografia, espaçamentos e padrões de componentes.
* [ ] **ID 07** - Utiliza Sass (SCSS), aplicando variáveis, mixins e funções para modularização do código.
* [ ] **ID 08** - Aplica tipografia responsiva utilizando media queries ou função `clamp()`.
* [ ] **ID 09** - Aplica técnicas de responsividade em imagens utilizando `object-fit` e containers responsivos.
* [ ] **ID 10** - Otimiza imagens utilizando formatos modernos como WebP e carregamento adaptativo através de `srcset` ou `picture`.

---

## RA2 - Realizar tratamento de formulários e aplicar validações customizadas no lado cliente.

* [ ] **ID 11** - Implementa validação HTML nativa em formulários, utilizando campos obrigatórios, tipos e limites de caracteres.
* [ ] **ID 12** - Utiliza expressões regulares (REGEX) para validações customizadas, como e-mail, telefone e CEP.
* [ ] **ID 13** - Utiliza elementos de seleção em formulários, como checkbox, radio e select.
* [ ] **ID 14** - Implementa leitura e escrita no `localStorage` ou `sessionStorage` para persistência de dados do carrinho e informações temporárias.

---

## RA3 - Aplicar ferramentas para otimização do processo de desenvolvimento web.

* [ ] **ID 15** - Configura ambiente utilizando Node.js e NPM para gerenciamento de pacotes e dependências.
* [ ] **ID 16** - Utiliza boas práticas de versionamento com Git/GitHub, incluindo branches e `.gitignore`.
* [ ] **ID 17** - Mantém um `README.md` padronizado conforme o template da disciplina, contendo documentação e checklist.
* [ ] **ID 18** - Organiza os arquivos do projeto de forma modular e estruturada.
* [ ] **ID 19** - Configura linters e formatadores, como ESLint e Prettier, para manter a qualidade e padronização do código.

---

## RA4 - Aplicar bibliotecas de funções e componentes em JavaScript para aprimorar a interatividade de páginas web.

* [ ] **ID 20** - Utiliza jQuery para manipulação do DOM e implementação de interações e eventos.
* [ ] **ID 21** - Integra e configura plugins JavaScript/jQuery relevantes para a aplicação, como máscaras de campos e componentes interativos.

---

## RA5 - Efetuar requisições assíncronas para uma API fake e APIs públicas, permitindo a obtenção e manipulação de dados dinamicamente.

* [ ] **ID 22** - Realiza requisições assíncronas para uma API Fake utilizando JSON Server para persistência de dados.
* [ ] **ID 23** - Realiza requisições assíncronas para uma API Fake para exibição dinâmica dos produtos na página.
* [ ] **ID 24** - Realiza requisições assíncronas para APIs públicas reais, exibindo os dados e tratando possíveis erros.

---

# 🚀 Manual de Execução

### 1. Clonar o repositório

Clone o projeto utilizando o Git:

```bash
git clone URL_DO_REPOSITORIO
```

### 2. Acessar o diretório

```bash
cd flora-urbana
```

### 3. Abrir o projeto no Visual Studio Code

Abra o diretório raiz do projeto no **Visual Studio Code**.

### 4. Abrir o terminal

Abra um terminal pelo VS Code ou qualquer terminal do sistema operacional, apontando para o diretório raiz do projeto.

### 5. Instalar as dependências

Execute:

```bash
npm i
```

As dependências necessárias serão instaladas de acordo com o arquivo `package.json`.

### 6. Executar a API Fake

O projeto utiliza o **JSON Server** para simular uma API REST.

Caso esteja configurado um script no `package.json`, execute:

```bash
npm run json:server
```

Ou, caso seja necessário executar diretamente:

```bash
npx json-server --watch db.json --routes routes.json
```

Por padrão, o JSON Server será executado em:

```text
http://localhost:3000
```

### 7. Executar o frontend

Para executar o frontend, abra o arquivo:

```text
index.html
```

ou utilize uma extensão como **Live Server** no Visual Studio Code.

A aplicação estará disponível em um endereço semelhante a:

```text
http://127.0.0.1:5500/
```

---

# 🗃️ API Fake

A API Fake é responsável por disponibilizar os dados utilizados pela aplicação.

Exemplo de estrutura do arquivo `db.json`:

```json
{
  "produtos": [
    {
      "id": 1,
      "nome": "Costela-de-Adão",
      "categoria": "Plantas",
      "preco": 89.90,
      "descricao": "Planta ornamental ideal para ambientes internos.",
      "imagem": "img/produtos/costela-de-adao.jpg",
      "estoque": 10
    },
    {
      "id": 2,
      "nome": "Jiboia",
      "categoria": "Plantas",
      "preco": 49.90,
      "descricao": "Planta de fácil cultivo e ótima para ambientes internos.",
      "imagem": "img/produtos/jiboia.jpg",
      "estoque": 15
    }
  ]
}
```

### Principais rotas

| Método   | Rota            | Descrição                      |
| -------- | --------------- | ------------------------------ |
| `GET`    | `/produtos`     | Lista todos os produtos        |
| `GET`    | `/produtos/:id` | Consulta um produto específico |
| `POST`   | `/produtos`     | Cadastra um novo produto       |
| `PUT`    | `/produtos/:id` | Atualiza um produto            |
| `DELETE` | `/produtos/:id` | Remove um produto              |

---

# 🌱 Objetivo da Flora Urbana

A **Flora Urbana** busca unir tecnologia e natureza através de uma experiência de compra digital simples, agradável e acessível.

O projeto também tem como finalidade aplicar, de maneira prática, conceitos de **desenvolvimento web, responsividade, JavaScript, consumo de APIs, manipulação do DOM, validação de formulários, armazenamento local e organização de projetos utilizando Git/GitHub**.

---

## 👩‍💻 Desenvolvimento

Projeto desenvolvido para fins acadêmicos, com foco na aplicação prática dos conhecimentos adquiridos durante a disciplina de desenvolvimento web.

**Flora Urbana — trazendo mais verde para o seu espaço. 🌿**
