
# 📄 Product Requirements Document (PRD) - Flora Urbana

## 1. Visão Geral e Objetivo

A **Flora Urbana** é uma aplicação web de e-commerce desenvolvida para simular uma loja virtual especializada na venda de **plantas, vasos, acessórios e produtos relacionados à jardinagem e decoração**.

O objetivo principal do sistema é proporcionar ao usuário uma experiência de compra **simples, intuitiva, agradável e responsiva**, permitindo que ele navegue pelo catálogo, conheça os produtos disponíveis, consulte seus detalhes, adicione itens ao carrinho e avance até a etapa de checkout.

**A Regra de Negócio Principal:** o sistema deve controlar o fluxo de compra desde a seleção dos produtos até a finalização do pedido, garantindo que os valores, quantidades, estoque e informações fornecidas pelo cliente sejam devidamente validados.

A aplicação possui caráter **didático e acadêmico**, tendo como finalidade aplicar conceitos de desenvolvimento web, incluindo criação de interfaces responsivas, manipulação do DOM, validação de formulários, armazenamento local e consumo de uma API Fake.

---

## 2. Atores do Sistema

* **Visitante:** Usuário que acessa a Flora Urbana sem realizar autenticação e pode navegar pelo catálogo, pesquisar produtos e consultar seus detalhes.

* **Cliente:** Usuário que seleciona produtos, adiciona itens ao carrinho, informa seus dados de entrega e realiza a simulação de uma compra.

* **Administrador / Sistema:** Responsável pela disponibilização e gerenciamento dos produtos através da API Fake, incluindo informações como nome, preço, categoria, descrição, imagem e estoque.

---

## 3. Histórias de Usuário e Escopo

Abaixo estão as funcionalidades principais do MVP (Minimum Viable Product), escritas sob a perspectiva do usuário final.

### 🏠 Épico 1: Navegação e Catálogo de Produtos

* **US01 - Acessar a Página Inicial:** Como um Visitante, quero acessar a página inicial da Flora Urbana para conhecer a loja, suas categorias e produtos e
