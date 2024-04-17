# Conceitos

- o design system é dividido em varios pacote
  - pacote de tokens
    - aqui fica as cores, fontes de todo projeto

-Monorepo

    - pratica de colocar vários projetos dentro de um unico repositorio/pasta de codigo que tem dependencias entre si

# aprendizados

- gerar package: npm init -y
- gerar tsconfig:

  - npm i typescript -D
  - npx tsc --init

- build pacote
  -TSUP: converte nosso código de TS para JS que será usado por outras aplicações // script de build inserido no pachage

# configurando pacotes

# react

- add: npm i -D react @types/react @types/react-dom
- radix: usado para desenvolver alguns components
  - lembrando que o radix permite customizar totalmente os components
- components desenvolvidos:
  - Button
  - text
  - Box
  - Heading
  - TextInput
  - TextArea
  - checkbox
  - MultiStep

# docs

- instalando o storybook: https://efficient-sloth-d85.notion.site/Atualiza-o-Storybook-v6-v7-42c254c66e584df3b9633334a563a51b ou https://www.notion.so/Atualiza-o-Storybook-v6-v7-a16e9ecbc31d4c4182322e09081c8c8e

# packages

- TurboRepo: util quando se trabalhar com monorepos. Ele ajuda a executar scripts em todos pacotes ao mesmo tempo. (Rodar todos pacotes do monorepo ao mesmo tempo)
  - configuração: turbo.json

# DEPLOY -

- npm i @storybook/storybook-deployer --save-dev
- gh repo create
- configuração no arquivo: deploy-docs.yml
- add config em main.js
  viteFinal: (config, { configType }) => {
  if (configType === 'PRODUCTION') {
  config.base = '/05-design-system/'
  }

  return config
  }
