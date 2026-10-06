# 🌐 Plataforma Web Institucional - Nossa ONG

Este repositório contém a interface web completa e responsiva desenvolvida para o ecossistema digital de uma Organização Não Governamental (ONG). O projeto foi construído focando em **arquitetura semântica**, **acessibilidade digital (WCAG)**, **validação nativa de dados** e **design modular**.

## 🚀 Demonstração
O projeto está publicado e pode ser acessado em tempo real através do GitHub Pages.

## 🎯 Objetivos da Etapa Concluída
- **Estruturação Semântica:** Implementação de layouts baseados em tags estruturais do HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`) garantindo significado computacional para leitores de tela e robôs de busca (SEO).
- **Hierarquia de Informação:** Aplicação lógica e estritamente sequencial de cabeçalhos (`<h1>` a `<h6>`).
- **Acessibilidade Dinâmica:** Inclusão de atributos `alt` descritivos em mídias e vinculação correta de elementos `<label>` através do atributo `for`.
- **Formulários Interativos Avançados:** Criação de agrupamentos lógicos com `<fieldset>` e `<legend>`, além do uso de expressões regulares (`pattern`) para máscaras e validações nativas em território nacional (CPF, CEP e Telefone).
- **Estilização e Design System:** Arquitetura visual centralizada em CSS externo para consistência de cores institucionais, tipografia e responsividade.

## 📂 Estrutura de Diretórios Organizacional

A árvore de arquivos do projeto segue o padrão profissional de separação de responsabilidades (Marcação vs. Recursos Estáticos):

```text
html-css-aula/
│
├── index.html           # Página Inicial (Apresentação institucional e contato)
├── projetos.html        # Detalhamento de projetos, voluntariado e doações
├── cadastro.html        # Formulário interativo de captação de apoiadores
├── README.md            # Documentação técnica do repositório
│
└── assets/              # Recursos globais da aplicação
    ├── css/
    │   └── estilos.css  # Centralização de regras visuais, resets e layout
    └── images/
        └── imagem-ong.jpg # Mídias locais vinculadas semanticamente
```

## 🛠️ Tecnologias Empregadas
- **HTML5:** Estrutura e engenharia de validação passiva na camada do cliente.
- **CSS3:** Estilização baseada em Box Model, Flexbox e boas práticas de contraste.
- **Git & GitHub:** Controle de versionamento e deploy automatizado.

## 🛡️ Engenharia de Validação de Dados (cadastro.html)
Para mitigar o envio de dados nulos ou mal formatados ao servidor (Back-end), o formulário implementa restrições nativas do HTML5:
* **CPF:** Máscara estrita via `pattern="\d{3}\.\d{3}\.\d{3}-\d{2}"` (Formato: 000.000.000-00).
* **CEP:** Máscara postal via `pattern="\d{5}-\d{3}"` (Formato: 00000-000).
* **Telefone:** Validação de telefonia móvel via `pattern="\(\d{2}\)\s9\d{4}-\d{4}"` (Formato: (11) 99999-9999).
* **Obrigatoriedade:** Atributo `required` injetado em campos estruturais de negócio.

---
*Nota: Este projeto foi validado utilizando o W3C Markup Validation Service, estando em total conformidade com os padrões internacionais da Web.*
