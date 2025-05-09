# 📰 Blog Bill Gates

Bem-vindo(a) ao repositório do **Blog Bill Gates**, um site baseado em **GitHub Pages** que divulga notícias, artigos e reflexões sobre tecnologia, inovação e filantropia, inspirado na visão e trabalho de Bill Gates.

---

## 📋 Sumário

* [Descrição do Projeto](#descrição-do-projeto)
* [Demo ao Vivo](#demo-ao-vivo)
* [Motivação](#motivação)
* [Tecnologias Utilizadas](#tecnologias-utilizadas)
* [Como Rodar Localmente](#como-rodar-localmente)
* [Estrutura de Pastas](#estrutura-de-pastas)
* [Personalização de Temas](#personalização-de-temas)
* [Scripts Disponíveis](#scripts-disponíveis)
* [Deploy Automático](#deploy-automático)
* [Contribuições](#contribuições)
* [Licença](#licença)

---

## 📄 Descrição do Projeto

O **Blog Bill Gates** é um site estático hospedado via GitHub Pages. Ele fornece:

* Páginas de artigos e notícias sobre tecnologia, saúde global e educação.
* Layout responsivo para desktop e mobile.
* Navegação intuitiva com barra lateral e menu superior.
* Recursos de acessibilidade.

---

## 🔗 Demo ao Vivo

Confira em: [https://caiooham.github.io/Blog-Bill-Gates/](https://caiooham.github.io/Blog-Bill-Gates/)

---

## 🎯 Motivação

Este projeto serve para:

1. Praticar GitHub Pages e Jekyll/Hugo (ou framework estático adotado).
2. Compartilhar conteúdo de valor sobre ciência e tecnologia.
3. Aprimorar habilidades em HTML, CSS e JavaScript.

---

## ⚙️ Tecnologias Utilizadas

* **GitHub Pages**: hospedagem estática gratuita.
* **Jekyll** (ou **Hugo**): gerador de site estático.
* **HTML5 & CSS3**: estrutura e estilo.
* **JavaScript**: interatividade (ex.: menu mobile, dark mode).
* **Bootstrap** (ou **Tailwind CSS**): framework de UI.
* **Font Awesome**: ícones.

---

## 🚀 Como Rodar Localmente

1. Clone o repositório:

   ```bash
   git clone https://github.com/caiooham/Blog-Bill-Gates.git
   cd Blog-Bill-Gates
   ```
2. Instale dependências (se usar Jekyll/Hugo):

   ```bash
   bundle install       # para Jekyll
   hugo server -D       # para Hugo
   ```
3. Inicie o servidor local:

   ```bash
   bundle exec jekyll serve
   # ou
   hugo server
   ```
4. Acesse `http://localhost:4000` no seu navegador.

---

## 📁 Estrutura de Pastas

```bash
Blog-Bill-Gates/
├── _config.yml         # Configurações do Jekyll
├── config.toml         # Configurações do Hugo (se aplicável)
├── _posts/             # Artigos em Markdown
├── assets/             # Imagens, CSS, JS
│   ├── css/
│   ├── js/
│   └── img/
├── _layouts/           # Templates HTML
├── _includes/          # Partes reutilizáveis (header, footer)
└── README.md           # Este arquivo
```

---

## 🎨 Personalização de Temas

Você pode alterar estilos editando os arquivos em `assets/css/`.
Para trocar cores ou fontes, ajuste as variáveis SASS (caso use) ou classes do framework.

---

## 📦 Scripts Disponíveis

| Comando          | Descrição                             |
| ---------------- | ------------------------------------- |
| `jekyll serve`   | Inicia servidor local Jekyll          |
| `hugo server -D` | Inicia servidor local Hugo com drafts |
| `npm run build`  | Gera arquivos de produção             |
| `npm run deploy` | Realiza deploy no GitHub Pages        |

---

## 🚀 Deploy Automático

O deploy é garantido via GitHub Actions. No push para a branch `main`, o workflow:

1. Instala dependências.
2. Gera o site estático.
3. Publica em `gh-pages`.

```yaml
# .github/workflows/deploy.yml
name: Deploy GitHub Pages
on:
  push:
    branches:
      - main
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: helaili/jekyll-action@v2   # ou Hugo action
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./_site
```
---
## 🤝 Contribuições
1. Fork este repositório.
2. Crie uma branch com sua feature: `feature/nome-da-feature`.
3. Commit suas alterações: `git commit -m 'Adiciona nova feature'`.
4. Push na branch: `git push origin feature/nome-da-feature`.
5. Abra um Pull Request.



