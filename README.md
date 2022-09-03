# cadl-openapi3-demo

Demo project for OpenAPI v3 emitter for Cadl

# Setup

Install the cadl compiler.

```bash
npm install -g @cadl-lang/compiler
```

Create a folder for your new Cadl project.

Initialize your project with

```bash
cadl init
```

At the prompts, select
- "Generic REST API"
- The name you want to use for your project
- The openapi3 library, "@cadl-lang/openapi3"

Install the packages:

```bash
npm install
```

Fix "Current Cadl compiler conflicts with local version" problem in VSCode:

- Set the `cadl-server-path` in your workspace settings to "${workspaceRoot}/node_modules/.bin/cadl-server"
- Restart VSCode.

Put your program in main.cadl

Add to your package.json:
```json
  "scripts": {
    "build": "cadl compile main.cadl --output-path ."
  },
```

Build the project and emit to `openapi.json`.

```bash
npm run build
```