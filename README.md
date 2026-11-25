# TechPulse — Página Inicial (MVP Front-End)

Primeira versão funcional da página inicial do **TechPulse**, portal de notícias de tecnologia construído com separação estrita entre estrutura (`index.html`), apresentação (`css/styles.css`) e documentação (`README.md`), com abordagem *mobile-first*, estética minimalista e foco em acessibilidade web.

---

## 1. Especificações Técnicas e Justificativas

### Paleta de cores e regra 60-30-10 (Hexadecimal e RGBA)
* **60% — Superfícies claras e respiro (`#ffffff` e `#fafafa`)**: o fundo branco puro na página e o cinza muito claro (`#fafafa`) em blocos de apoio garantem amplo espaço em branco e leitura limpa sem poluição visual.
* **30% — Estrutura, tipografia e bordas (`#111827`, `#4b5563` e `#e5e7eb`)**: o grafite escuro (`#111827`) entrega alto contraste na leitura e estrutura o rodapé; o cinza intermediário (`#4b5563`) organiza subtítulos, legendas e links secundários; as bordas sutis (`#e5e7eb`) delimitam áreas com leveza.
* **10% — Destaque e ação (`#2563eb`, `rgba(37, 99, 235, 0.88)`, `rgba(37, 99, 235, 0.08)` e `rgba(37, 99, 235, 0.25)`)**: o azul é reservado ao botão de ação (`.btn-acao`), ao foco/hover e a detalhes pontuais, enquanto as variações em `rgba()` criam camadas semitransparentes suaves no selo editorial e nos estados interativos.

### Tipografia e alinhamento
* **Família tipográfica**: pilha *sans-serif* (`"Inter", "Segoe UI", Roboto, Helvetica, Arial, sans-serif`) com traços limpos, excelente legibilidade em telas pequenas e carregamento rápido sem depender de fontes pesadas.
* **Tamanho e hierarquia**: `<h1>` em `1.875rem` no mobile e `2.35rem` em telas `>= 768px`, `<h2>` em `1.0625rem`–`1.25rem` e corpo de texto em `1rem` com `line-height: 1.7` para favorecer a leitura contínua.
* **Alinhamento**: textos principais, títulos, listas e botão alinhados à esquerda (`text-align: left`) para facilitar o escaneamento visual; avisos do rodapé centralizados (`text-align: center`).

### Espaçamentos e Box Model (`margin`, `border`, `padding`)
* **`box-sizing: border-box`**: garante que `padding` e `border` entrem no cálculo da largura total, evitando estouros horizontais em telas estreitas.
* **`padding`**: cria respiro interno em `.container` (`24px` no mobile, `32px` no desktop), em `.midia-artigo` (`14px`–`16px`), nos itens de `.lista-tecnologias` (`14px 16px`) e em `.btn-acao` (`12px 22px`).
* **`margin`**: estabelece ritmo vertical entre cabeçalho, conteúdo principal, blocos do artigo e rodapé (`margin-bottom` e `margin-top` generosos para manter bastante espaço em branco).
* **`border`**: define divisórias discretas (`1px solid #e5e7eb`), acento lateral nos itens da lista (`3px solid #111827`), borda de `2px` no botão `.btn-acao` e faixa inferior de `3px` no rodapé.

---

## 2. Tecnologias e Serviços Utilizados

* **HTML5 semântico**: estrutura com `<!DOCTYPE html>`, `<head>`, `<body>`, `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<figure>`, `<figcaption>` e `<footer>`, além de `alt` descritivo na imagem e `aria-label` na navegação.
* **CSS3 externo (`css/styles.css`)**: variáveis `:root`, seletores de tag, classe reutilizável (`.btn-acao`), ID exclusivo (`#cabecalho-principal`), Flexbox, Box Model e media query *mobile-first* (`@media (min-width: 768px)`).
* **Serviços externos**:
  * **Unsplash**: entrega da imagem ilustrativa de infraestrutura tecnológica.
  * **GitHub**: hospedagem e versionamento público do repositório para correção.

---

## 3. Sitemap Visual, Hierarquia de Conteúdo e Taxonomia

### Hierarquia de Conteúdo e Taxonomia
* **Hierarquia de conteúdo**: a **Página Inicial** ocupa o nível superior e organiza o fluxo de leitura da identidade e navegação (`<header>` e `<nav>`) para a reportagem principal e tecnologias em destaque (`<main>`, `<article>` e `<section>`), encerrando na identificação institucional (`<footer>`).
* **Taxonomia**: o conteúdo é classificado em espaços temáticos de tecnologia e subcategorias específicas para orientar a navegação e a expansão editorial do portal.

### Diagrama do Sitemap Visual

```text
                        [ Página Inicial (Home) ]
                                    |
        +---------------------------+---------------------------+
        |                           |                           |
        v                           v                           v
[ 1. Engenharia e Web ]     [ 2. Infraestrutura ]       [ 3. Produto e UX ]
   |-- Arquitetura Front-End     |-- Edge & CDN                |-- Design Systems
   |-- Performance & Vitals      |-- Cloud & Observabilidade   |-- Acessibilidade Web
   |-- HTML5 & CSS3 Padrões      |-- Segurança de Aplicações   |-- Pesquisa de Usuário
```