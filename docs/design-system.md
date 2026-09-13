# 🎨 Design System - Flora Urbana

Neste projeto, utilizamos um framework UI como base e aplicamos customizações para refletir a identidade visual da **Flora Urbana**, priorizando uma experiência de compra agradável, natural, moderna e intuitiva.

---

### 1. Framework Base

* **Framework escolhido:** MaterializeCSS
* **Motivação:** Oferece componentes prontos baseados no Material Design, facilitando a criação de interfaces responsivas, organizadas e consistentes. A utilização do framework permite acelerar o desenvolvimento e manter um padrão visual entre as diferentes páginas da aplicação.

---

### 2. Paleta de Cores (Customização)

A paleta de cores da Flora Urbana foi inspirada na natureza, principalmente em tons de verde, bege e branco. O objetivo é transmitir sensações de frescor, tranquilidade, cuidado e proximidade com as plantas.

* **Cor Primária (Verde Natureza):** `#2E7D32` *(Green darken-2)*

  * **Uso:** Botões principais, links de destaque, elementos de navegação selecionados e ações relacionadas à compra.
  * **Objetivo:** Representar a natureza e reforçar a identidade da marca.

* **Cor Secundária (Verde Folha):** `#558B2F` *(Light Green darken-3)*

  * **Uso:** Ícones, detalhes visuais, categorias, elementos secundários e estados de interação.
  * **Objetivo:** Complementar a cor primária e reforçar a temática natural.

* **Cor de Fundo (Creme):** `#FAF8F3`

  * **Uso:** Fundo geral das páginas e áreas de conteúdo.
  * **Objetivo:** Criar uma aparência mais acolhedora e destacar os produtos sem utilizar um branco excessivamente frio.

* **Cor de Superfície (Branco):** `#FFFFFF`

  * **Uso:** Cards, formulários, menus, áreas de produtos e componentes que precisam de destaque sobre o fundo.
  * **Objetivo:** Garantir contraste e facilitar a leitura.

* **Cor de Texto Principal:** `#263238`

  * **Uso:** Títulos, descrições, informações dos produtos e textos de maior importância.
  * **Objetivo:** Proporcionar boa legibilidade sem utilizar o preto absoluto.

* **Cor de Texto Secundário:** `#607D8B`

  * **Uso:** Informações complementares, textos auxiliares, preços anteriores e descrições secundárias.

* **Cor de Sucesso:** `#388E3C`

  * **Uso:** Confirmações de compra, mensagens de sucesso, disponibilidade de produtos e operações concluídas.
  * **Exemplo:** "Produto adicionado ao carrinho."

* **Cor de Alerta:** `#F9A825`

  * **Uso:** Avisos relacionados a estoque, informações importantes e situações que exigem atenção.
  * **Exemplo:** "Últimas unidades disponíveis."

* **Cor de Erro:** `#C62828`

  * **Uso:** Erros de preenchimento, falhas de validação e mensagens de operação não concluída.
  * **Exemplo:** "Informe um endereço válido."

---

### 3. Tipografia

A tipografia deve transmitir modernidade e simplicidade, mantendo boa legibilidade em computadores, tablets e dispositivos móveis.

As fontes podem ser importadas via Google Fonts para manter uma identidade visual consistente.

* **Títulos (H1 a H6):** `Poppins, sans-serif`

  * **Peso:** 600 ou 700
  * **Uso:** Títulos de páginas, nomes de seções e chamadas de destaque.
  * **Objetivo:** Criar uma aparência moderna e amigável.

* **Textos Corridos:** `Open Sans, sans-serif`

  * **Peso:** 400
  * **Uso:** Descrições, textos informativos, menus e conteúdos gerais.

* **Botões e Elementos de Interface:** `Open Sans, sans-serif`

  * **Peso:** 600
  * **Uso:** Botões, filtros, opções de navegação e ações do usuário.

* **Preços:** `Poppins, sans-serif`

  * **Peso:** 600 ou 700
  * **Uso:** Exibição dos valores dos produtos e do total do carrinho.
  * **Objetivo:** Facilitar a identificação das informações financeiras durante a compra.

---

### 4. Diretrizes de Uso de Componentes

As customizações dos componentes do MaterializeCSS devem seguir a identidade visual da Flora Urbana e manter a experiência de compra simples e intuitiva.

#### Botões (`.btn`)

Os botões devem apresentar claramente a ação que será executada.

* **Ação principal:** utilizar a cor primária `#2E7D32`.

  * Exemplos: "Adicionar ao carrinho", "Comprar agora", "Finalizar pedido".

* **Ação secundária:** utilizar `.btn-flat` ou uma variação visual mais discreta.

  * Exemplos: "Continuar comprando", "Voltar".

* **Ações de confirmação:** utilizar a cor de sucesso quando necessário.

* **Ações destrutivas:** utilizar a cor de erro com moderação.

  * Exemplo: "Remover produto".

Os botões devem possuir tamanho suficiente para facilitar a interação em dispositivos móveis.

---

#### Cards (`.card`)

Os cards são utilizados como principal componente para apresentação dos produtos.

Cada card de produto deve apresentar, preferencialmente:

* Imagem do produto;
* Nome;
* Categoria;
* Preço;
* Indicador de disponibilidade;
* Botão "Adicionar ao carrinho" ou "Ver detalhes".

Os cards devem possuir:

* Fundo branco;
* Cantos levemente arredondados;
* Sombra discreta;
* Espaçamento interno adequado;
* Imagem com proporção consistente.

O objetivo é criar uma apresentação visual limpa, semelhante a lojas virtuais modernas.

---

#### Imagens de Produtos

As imagens possuem papel importante na experiência da Flora Urbana.

As imagens devem:

* Ter boa resolução;
* Utilizar proporções consistentes;
* Possuir bordas ou cantos arredondados quando apropriado;
* Ser apresentadas em destaque nos detalhes do produto;
* Possuir `alt` descritivo para acessibilidade.

Sempre que possível, deve-se evitar imagens visualmente muito diferentes entre os produtos para manter a consistência do catálogo.

---

#### Barra de Navegação (`.navbar`)

A barra de navegação deve ser simples e objetiva.

Deve conter, conforme a página:

* Logo/nome da Flora Urbana;
* Link para início;
* Link para produtos;
* Campo ou acesso à busca;
* Ícone/link do carrinho;
* Quantidade de produtos no carrinho, quando aplicável.

A navegação deve utilizar a cor primária ou uma tonalidade escura de verde, garantindo contraste adequado com os textos.

---

#### Formulários (`.input-field`)

Os formulários devem possuir aparência limpa e organizada.

Devem ser utilizados para:

* Cadastro de cliente;
* Informações de contato;
* Endereço de entrega;
* Seleção da forma de pagamento;
* Seleção da forma de entrega.

Diretrizes:

* Labels sempre visíveis ou corretamente associadas aos campos;
* Campos com largura adequada;
* Mensagens de erro próximas ao campo correspondente;
* Indicação clara dos campos obrigatórios;
* Validação antes da finalização do pedido.

---

#### Filtros e Busca

A busca e os filtros devem facilitar a localização dos produtos.

Os filtros podem incluir:

* Categoria;
* Faixa de preço;
* Disponibilidade;
* Ordenação por preço ou nome.

Os controles devem ser simples e não ocupar espaço excessivo na interface.

---

#### Carrinho de Compras

O carrinho deve apresentar de maneira clara:

* Imagem do produto;
* Nome;
* Preço unitário;
* Quantidade;
* Subtotal;
* Opção para alterar quantidade;
* Opção para remover o item;
* Total da compra;
* Valor do frete;
* Total final.

O usuário deve conseguir identificar facilmente o valor total antes de prosseguir para o checkout.

---

#### Checkout

O checkout deve ser dividido em etapas ou seções visualmente organizadas:

1. Dados do cliente;
2. Endereço de entrega;
3. Forma de entrega;
4. Forma de pagamento;
5. Resumo do pedido;
6. Confirmação.

A interface deve evitar informações desnecessárias e destacar as informações essenciais para conclusão da compra.

---

#### Mensagens e Feedback

O sistema deve informar claramente o resultado das ações realizadas pelo usuário.

* **Sucesso:** verde (`#388E3C`)

  * "Produto adicionado ao carrinho."
  * "Pedido realizado com sucesso."

* **Alerta:** amarelo (`#F9A825`)

  * "Restam poucas unidades."

* **Erro:** vermelho (`#C62828`)

  * "Não foi possível adicionar o produto."
  * "Preencha os campos obrigatórios."

As mensagens devem ser objetivas e fáceis de compreender.

---
