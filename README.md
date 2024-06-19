# Astro Starter Kit: Basics

```sh
npm create astro@latest -- --template basics
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/basics)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/basics)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/basics/devcontainer.json)

> 🧑‍🚀  Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |



## UML
```mermaid
sequenceDiagram
    participant User
    participant System

    User->>System: Enter API Key
    User->>System: Upload PDF/PDF URL
    User->>System: Ask Question
    User->>System: Submit Call to Action

    System->>System: Blank field Validations
    System->>System: Convert PDF to Text
    System->>System: Decompose Text to Chunks (150 word length)
    System->>System: Check if embeddings file exists
    System->>System: If file exists, load embeddings and set the fitted attribute to True
    System->>System: If file doesn't exist, generate embeddings, fit the recommender, save embeddings to file and set fitted attribute to True
    System->>System: Perform Semantic Search and return Top 5 Chunks with KNN
    System->>System: Load Open AI prompt
    System->>System: Embed Top 5 Chunks in Open AI Prompt
    System->>System: Generate Answer with Davinci

    System-->>User: Return Answer

