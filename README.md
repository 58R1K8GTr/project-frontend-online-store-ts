# 🛒 Front-end Online Store

O **Front-end Online Store** é uma aplicação de e-commerce simplificada que simula o ecossistema de uma loja online dinâmica. Desenvolvida em React, a plataforma interage diretamente com a API do Mercado Livre para busca de produtos e filtragem por categorias em tempo real. Os usuários podem explorar itens de forma resumida ou detalhada, gerenciar dinamicamente um carrinho de compras e simular o fluxo de finalização do pedido.

Este projeto foi construído colaborativamente em um ambiente de equipe que simulou cenários reais do mercado de trabalho.

---

## 🚀 Habilidades e Aprendizados Desenvolvidos

Este repositório consolida o aprendizado de arquitetura front-end assíncrona e práticas avançadas de desenvolvimento colaborativo:

### 👥 Metodologias Ágeis e Trabalho em Equipe
*   **Frameworks Scrum e Kanban:** Implementação e vivência prática das rotinas ágeis para organização de tarefas.
*   **Gestão Visual com Trello:** Utilização ativa de quadros Kanban duplicados e customizados para distribuição de demandas e acompanhamento do progresso das tarefas.
*   **Priorização Baseada em Valor (Grooming):** Compreensão de requisitos estruturados por dependências e prioridades lógicas, reduzindo significativamente conflitos de código (*merge conflicts*).

### 🛠️ Engenharia de Software & Front-end
*   **Consumo Assíncrono de APIs Rest:** Manipulação estruturada de requisições HTTP utilizando a API nativa *Fetch* para integração com os endpoints do Mercado Livre.
*   **Componentização e Rotas Dinâmicas:** Uso avançado de ecossistema React (`BrowserRouter`) para criar transições fluidas entre catálogo, detalhes e carrinho.
*   **Gerenciamento de Fluxo e Estado:** Tráfego inteligente de propriedades (`props`) e persistência pontual em cache local (`localStorage`) para garantir a consistência das informações do carrinho.
*   **Qualidade e Padrões de Código:** Uso rigoroso do *ESLint* para garantir a manutenibilidade, legibilidade e conformidade com as boas práticas de desenvolvimento JS/TS.
*   **Testes de Comportamento (RTL):** Validação de fluxos de usuário por meio da *React Testing Library*, mapeando elementos por meio de seletores semânticos específicos (`data-testid`).

---

## 💻 O que foi Desenvolvido

A aplicação é segmentada por um fluxo lógico de aquisição de produtos estruturado nas seguintes features:

### 🔍 1. Módulo de Serviços da API
*   Concentração das chamadas externas no arquivo `src/services/api.js`.
*   Função `getCategories()` mapeando dinamicamente as categorias de produto do Mercado Livre.
*   Função `getProductsFromCategoryAndQuery(categoryId, query)` estruturando a lógica condicional necessária para buscar produtos por termo, categoria isolada ou ambos simultaneamente.

### 🏠 2. Catálogo Dinâmico (Página Inicial)
*   **Listagem Receptiva:** Uma interface limpa exibindo inicialmente a mensagem explicativa: *"Digite algum termo de pesquisa ou escolha uma categoria."*.
*   **Busca por Termo:** Caixa de busca interativa que consulta a API e renderiza cartões de produtos com nome, imagem e preço. Em caso de ausência de dados, sinaliza *"Nenhum produto foi encontrado"*.
*   **Filtros por Categoria:** Painel lateral alimentado via API que atualiza instantaneamente a vitrine de produtos de acordo com a categoria selecionada.

### 🛍️ 3. Carrinho de Compras Interativo
*   **Navegação Rápida:** Botão de acesso ao carrinho fixado globalmente nas principais telas.
*   **Lógica de Persistência:** Adição de produtos diretamente a partir da vitrine principal ou da página de visualização detalhada.
*   **Controle Quantitativo:** Visualização de itens contendo título, preço total consolidado e a quantidade de cada unidade adicionada, operando de forma integrada com o `localStorage`.

### 📄 4. Página de Detalhes do Produto
*   Redirecionamento ao clicar em qualquer produto da página principal para um ambiente imersivo.
*   Exibição em alta fidelidade do nome, imagens, preço e especificações técnicas do item selecionado, permitindo o envio do item ao carrinho ali mesmo.

---

## 🔌 Endpoints Utilizados da API do Mercado Livre

A aplicação consome a infraestrutura pública do Mercado Livre através dos seguintes caminhos:

| Funcionalidade | Endpoint da Requisição |
| :--- | :--- |
| **Listar Categorias** | `https://api.mercadolibre.com/sites/MLB/categories` |
| **Busca por Termo** | `https://api.mercadolibre.com/sites/MLB/search?q=$QUERY` |
| **Busca por Categoria** | `https://api.mercadolibre.com/sites/MLB/search?category=$CATEGORY_ID` |
| **Busca Combinada** | `https://api.mercadolibre.com/sites/MLB/search?category=$CATEGORY_ID&q=$QUERY` |
| **Detalhes do Produto** | `https://api.mercadolibre.com/items/$PRODUCT_ID` |

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

*   **React** (com suporte de ciclo de vida e gerenciamento de estados locais)
*   **React Router Dom** (Gerenciamento e encapsulamento de rotas)
*   **Fetch API** (Comunicação assíncrona baseada em Promises)
*   **React Testing Library (RTL)** & **Jest** (Testes unitários e comportamentais)
*   **ESLint** (Padronização e análise estática do código)
*   **Trello** (Ferramenta Kanban para gestão das demandas da equipe)
*   **Figma** (Utilizado opcionalmente como guia de prototipagem e UI/UX)

---

## 🔧 Scripts de Execução Local

1. Clonar o repositório e entrar na pasta correspondente:
   ```bash
   git clone git@github.com:seu-usuario/sd-0x-project-frontend-online-store.git
   cd sd-0x-project-frontend-online-store
