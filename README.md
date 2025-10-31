# 💻 Projeto Profissional de Desenvolvimento Web Acessível e Otimizado

## 📄 Visão Geral

Este projeto tem como objetivo demonstrar a aplicação de **práticas profissionais obrigatórias** em um ciclo de desenvolvimento de software, abrangendo desde o controle de versão e acessibilidade (WCAG 2.1 AA) até a otimização de deploy para ambiente de produção.

A entrega final comprova o domínio nas áreas de **DevOps (versionamento)**, **Experiência do Usuário (Acessibilidade)** e **Performance Web**.

---

## 🚀 Requisitos e Implementação

Os seguintes requisitos foram abordados e implementados neste repositório:

### 1. 🌲 Controle de Versão (Git/GitHub)

O fluxo de trabalho segue o padrão **GitFlow**, garantindo um ambiente de desenvolvimento robusto e rastreável.

#### Estratégia de Branching

* **`main`**: Contém o código de produção (pronto para deploy). Apenas merges de `release/*` ou `hotfix/*` são permitidos.
* **`develop`**: Branch de integração estável. Todas as novas *features* são integradas aqui.
* **`feature/*`**: Branches criadas a partir de `develop` para desenvolvimento de novas funcionalidades.
* **`release/*`**: Branches criadas a partir de `develop` para preparação final de uma nova versão (testes, ajustes de documentação, etc.).
* **`hotfix/*`**: Branches criadas a partir de `main` para correção imediata de bugs críticos em produção.

#### Histórico de Commits e Releases

* **Commits Semânticos**: Utilizamos a especificação **Conventional Commits** para manter o histórico claro e automatizado.
    * Exemplos: `feat: Adiciona componente de navegação`, `fix: Corrige contraste do texto do rodapé`, `docs: Atualiza seção de deploy do README`.
* **Versionamento Semântico**: As releases são marcadas com tags (e.g., `v1.0.0`) e seguem o padrão MAJOR.MINOR.PATCH.
    * `MAJOR`: Mudanças incompatíveis (breaking changes).
    * `MINOR`: Adição de funcionalidades de forma retrocompatível.
    * `PATCH`: Correções de bugs retrocompatíveis.

| Tipo de Mudança | Exemplo de Commit | Regra de Incremento |
| :--- | :--- | :--- |
| Nova Funcionalidade | `feat: ...` | MINOR |
| Correção de Bug | `fix: ...` | PATCH |
| Mudança Incompatível | *Múltiplos commits* | MAJOR (na release) |

---

### 2. ♿ Acessibilidade (WCAG 2.1 Nível AA)

A acessibilidade foi integrada desde o início do desenvolvimento para garantir que a aplicação possa ser usada pelo maior número de pessoas possível.

| Requisito | Detalhamento da Implementação |
| :--- | :--- |
| **Navegação por Teclado** | Todos os elementos interativos são acessíveis via tecla **Tab** e **Shift+Tab**. O foco visível (`:focus`) foi estilizado de forma clara. |
| **Estrutura Semântica** | Uso de tags HTML5 como `<header>`, `<main>`, `<nav>`, `<footer>`, `<button>` e o uso correto de `role` e `aria` para aprimorar a estrutura. |
| **Contraste Mínimo** | O contraste de cores foi validado para atender ao mínimo de **4.5:1** para texto normal, conforme o nível AA. |
| **Suporte para Leitores de Tela** | Imagens importantes possuem atributos `alt` descritivos. Elementos complexos e *widgets* interativos utilizam o conjunto de atributos **ARIA** (Accessible Rich Internet Applications). |
| **Alto Contraste e Modo Escuro** | Implementação de um seletor de tema (``) que alterna entre o modo padrão, um modo de **Alto Contraste** (cores limitadas e alto contraste garantido) e um **Modo Escuro** acessível. |

---

### 3. ⚙️ Otimização para Produção (Deploy)

A aplicação foi preparada para um ambiente de produção, visando carregamento rápido e baixo consumo de banda.

* **Minificação de Assets:** O *pipeline* de *build* (e.g., Webpack/Gulp/Parcel) está configurado para minificar (remover espaços, comentários e otimizar) o código **HTML**, **CSS** e **JavaScript** antes do deploy.
* **Compressão de Imagens:** Todas as imagens utilizadas no projeto foram otimizadas (e.g., usando WebP ou compressão sem perda/com perdas mínimas) para reduzir o tempo de carregamento.

---

## 🛠️ Como Executar o Projeto Localmente

Siga os passos abaixo para configurar e executar a aplicação em seu ambiente local.

### Pré-requisitos

* [Node.js](https://nodejs.org/) (Versão LTS)
* [Git](https://git-scm.com/)

### Instalação

1.  **Clone o repositório:**
    ```bash
    git clone [Link do Repositório GitHub]
    cd [Nome da Pasta do Projeto]
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    # ou yarn install
    ```

3.  **Execute o projeto em modo de desenvolvimento:**
    ```bash
    npm run start
    # ou yarn start
    ```
    A aplicação estará acessível em `http://localhost:[PORTA]`.

4.  **Gere a versão de Produção (Otimizada):**
    ```bash
    npm run build
    # ou yarn build
    ```
    Os arquivos minificados e otimizados estarão disponíveis na pasta `/dist` ou `/build`.

---

## ✅ Entregáveis Finais

Este repositório serve como a entrega final e deve ser avaliado com base nos seguintes itens:

1.  **Repositório GitHub Completo:**
    * Código-fonte completo e funcional.
    * Histórico de **commits** semântico.
    * **Pull Requests** (PRs) e **Issues** devidamente utilizados.
    * **Tags** de versão semântica e **Releases** no GitHub.
2.  **Documentação Técnica:** Este arquivo `README.md` completo e profissional.
3.  **Conformidade:** Cumprimento de todos os requisitos de Acessibilidade (WCAG 2.1 AA) e Otimização para Produção.

---

## 🧑‍💻 Autores

Este projeto foi desenvolvido por:

* **[Nome Completo do Aluno 1]** - [@GitHubUsername1](https://github.com/GitHubUsername1)
* **[Nome Completo do Aluno 2]** - [@GitHubUsername2](https://github.com/GitHubUsername2)

## ⚖️ Licença

Este projeto está licenciado sob a Licença **MIT**. Veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.
