<h1 align="center"> Landing Page – Encantos Literários </h1>
<p align="center"> Página de apresentação de um clube de assinatura literário, construída com foco em responsividade avançada, microinterações e fidelidade máxima ao layout do Figma. <br> Desenvolvida como prática intensiva de <strong>HTML5 semântico, CSS modular, Grid, Flexbox, animações com transições suaves e padrões responsivos profissionais</strong>. </p>

<p align="center">
  <a href="#-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-projeto">Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-layout">Layout</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-estrutura">Estrutura</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-funcionalidades">Funcionalidades</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-aprendizados">Aprendizados</a>
</p>

<p align="center">
  <img alt="License" src="https://img.shields.io/static/v1?label=license&message=MIT&color=49AA26&labelColor=000000">
</p>

<br>

<p align="center">
  <img alt="capa do projeto" src="../assets/capa.png" width="100%">
</p>

---

## 🚀 Tecnologias

Esse projeto foi construído utilizando:

- **HTML5 semântico** – seções bem definidas (`header`, `main`, `section`, `footer`)
- **CSS3 modular** – arquivos separados por contexto (`global`, `hero`, `material`, `signature-plans`, `footer`)
- **Flexbox & Grid** – organização de layouts em coluna no mobile e em múltiplas colunas no desktop
- **Design System próprio** – tokens de cor, tipografia, espaçamento e componentes reaproveitáveis
- **SVG Icons** – ícones leves para redes sociais e elementos decorativos
- **Transições CSS** – animações suaves em botões, cards e ilustrações
- **Figma** – como referência visual com medidas e espaçamentos precisos
- **Git & GitHub** – versionamento e publicação do código

---

## 💻 Projeto

O objetivo do projeto é criar uma **landing page completa** para o clube de assinatura literário *Encantos Literários*, apresentando:

- proposta do clube
- benefícios do kit mensal
- planos de assinatura
- canais de contato e redes sociais

A página foi construída buscando **reproduzir o Figma com o máximo de precisão**, respeitando:

- espaçamentos verticais e horizontais
- hierarquia de títulos e textos
- estilo tipográfico do layout
- cores e gradientes
- posicionamento das ilustrações
- proporção dos cards de plano
- detalhes do footer (livro em perspectiva no fundo)

---

## 🎨 Layout

Algumas decisões visuais implementadas:

- **Paleta em tons de azul** com detalhes em rosa para destacar ações importantes
- **Hero** com chamada principal, descrição e CTA com microanimação no hover
- **Seção “Kit mensal” (#material)** com livro ilustrado e elementos “saindo” do kit (broche, marca-páginas, setas e labels)
- **Seção de planos (#signature-plans)** com cards em destaque, plano semestral como “popular” e variação de cores
- **Footer** com ilustração de livro abrindo, logo, redes sociais e colunas de links

### Responsividade

- **Mobile (375 px)**  
  - layout em coluna única  
  - cards de planos viram um **carrossel horizontal** com `scroll-snap`  
  - botões ocupam toda a largura útil  
  - espaçamentos adaptados para leitura confortável em tela pequena  

- **Desktop (1440 px)**  
  - hero centralizado com respiro lateral  
  - seção do kit com imagens posicionadas via `position: absolute` e labels ao redor do livro  
  - seção de planos em destaque com animação “leque” no hover  
  - footer alinhado por grid invisível, respeitando as distâncias do Figma (logo + ícones à esquerda, links à direita)

---

## 📚 Estrutura

A página está organizada em:

- `<header>` (dentro da seção hero)
  - logomarca em versão horizontal (desktop) e símbolo (mobile)
  - botão de ação “Assinar”

- `<main>`
  - **Seção Hero – `#hero`**
    - título e subtítulo
    - imagem de fundo aplicada via CSS
    - CTA com efeito circular no hover

  - **Seção Kit Mensal – `#material`**
    - título com ícone de estrela
    - parágrafo explicando o conteúdo do kit
    - livro central + broche + marca-páginas + setas e labels

  - **Seção Planos – `#signature-plans`**
    - título “Assinatura Encantos Literários”
    - wrapper com três cards de plano:
      - Mensal
      - Semestral (plano em destaque)
      - Anual
    - cada card contém:
      - nome do plano
      - preço principal (valor/mês)
      - preço anual equivalente
      - lista de benefícios com ícone de estrela
      - botão de assinatura

- `<footer id="site-footer">`
  - logo do clube
  - lista de ícones de redes sociais
  - coluna **Conteúdos**
  - coluna **Ajuda**

---

## 🔧 Funcionalidades

- **Layout totalmente responsivo** (mobile-first, com ajustes de desktop por media queries)
- **Hero com CTA animado**: efeito circular no hover usando pseudo-elemento `::before`
- **Seção “Kit mensal” animada**:
  - elementos do kit “saem de dentro” do livro ao passar o mouse no desktop  
  - transições suaves usando `transform` e `transition`
- **Planos com dois comportamentos**:
  - **Mobile**: carrossel horizontal com `overflow-x: auto` + `scroll-snap-type`
  - **Desktop**: card central em foco; cards laterais “saem de trás” dele no hover, levemente rotacionados
- **Plano semestral com estilo especial**:
  - cores diferenciadas de texto, ícones e botão
  - reflete o destaque visual do Figma (“Popular”)
- **Footer com imagem de fundo**:
  - ilustração do livro aplicada como `background-image`
  - ajuste de `background-size` para preencher a área sem distorções
- **Estados de hover**:
  - botões de plano com efeito circular
  - ícones de redes sociais trocando de cor
  - links do footer com mudança de cor para reforçar interatividade

---

## 🧪 Aprendizados

Durante o desenvolvimento deste projeto, foram praticados e reforçados:

- Criação de **layout mobile-first** com ajustes pontuais para desktop
- **Modularização do CSS**, separando cada seção em seu próprio arquivo
- Uso combinado de **Flexbox, Grid e `position: absolute`** para reproduzir layouts complexos
- Aplicação de **scroll snapping** para carrosséis suaves no mobile
- Animações usando apenas **CSS transitions e transforms**, evitando JS
- Controle de **z-index** e ordem de empilhamento para elementos que se sobrepõem
- Ajustes de medidas em **rem** a partir de valores em **px** do Figma
- Reutilização de tokens de cor, tipografia e espaçamento definidos no design system
- Refinos de alinhamento para ficar o mais próximo possível do layout original

---

## 📜 Licença

Esse projeto está sob a licença **MIT**.

---

✨ Desenvolvido com dedicação por **Fabiano Ferreira**.
