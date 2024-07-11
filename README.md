# Aya Vue3 extension Pack

A collection of extensions for working with Vue3 Applications in VS Code

These are some of my favorite extensions to make Vue application development easier and fun.



## Code Snippets

| Prefix/命令 | Method/方法名 | Description/用途 |
| --- | --- | --- |
| `vuets` | Vue3  Setup TypeScript Template | Quickly generate a Vue3 setup template with TypeScript(SCSS Scpoed)<br />快速生成一个Vue3的TypeScript的setup代码片段(SCSS Scpoed) |
| `vuejs` | Vue3  Setup JavaScript Template | Quickly generate a Vue3 setup template with JavaScript(SCSS Scpoed)<br />快速生成一个Vue3的JavaScript的setup代码片段(SCSS Scpoed) |
| `vue2js` | Vue2  Setup JavaScript Template | Quickly generate a Vue2 setup template with JavaScript(SCSS Scpoed)<br />快速生成一个Vue2的JavaScript的setup代码片段(SCSS Scpoed) |
| `vuedcjs` | Vue Javascript defineComponent Template |  Quickly generate a Vue defineComponent template with JavaScript(SCSS Scpoed)<br />快速生成一个Vue的defineComponent代码片段(SCSS Scpoed) |
| `vref` | Quick Created ref Object(Javascript) |  Quickly generate a ref object with JavaScript<br />快速生成一个ref对象 |
| `vproxy` | Get Current Proxy | Quick get current component proxy:`const { proxy } = getCurrentInstance()`<br />快速获取当前组件的proxy: `const { proxy } = getCurrentInstance()` |
| `vwatch` | Created Watch In Setup |  Quickly generate a watch in setup(deep watch)<br />快速生成一个setup的watch(深度监听) |
| `vcomputed` | Created Computed In Setup |  Quickly generate a computed in setup<br />快速生成一个setup的computed |

## VS Code Eslint Auto Fix Config

- Open project folder
- Prese down `F1`
- Paste `open workspace settings(JSON)` and prese down `Enter`
- Paste the content below 

```json5
{
  // Enable the ESlint flat config support
  "eslint.experimental.useFlatConfig": true,

  // Disable the default formatter, use eslint instead
  "prettier.enable": false,
  "editor.formatOnSave": false,

  // Auto fix
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.organizeImports": "never"
  },

  // Silent the stylistic rules in you IDE, but still auto fix them
  "eslint.rules.customizations": [
    { "rule": "style/*", "severity": "off" },
    { "rule": "format/*", "severity": "off" },
    { "rule": "*-indent", "severity": "off" },
    { "rule": "*-spacing", "severity": "off" },
    { "rule": "*-spaces", "severity": "off" },
    { "rule": "*-order", "severity": "off" },
    { "rule": "*-dangle", "severity": "off" },
    { "rule": "*-newline", "severity": "off" },
    { "rule": "*quotes", "severity": "off" },
    { "rule": "*semi", "severity": "off" }
  ],

  // Enable eslint for all supported languages
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "vue",
    "html",
    "markdown",
    "json",
    "jsonc",
    "yaml",
    "toml"
  ]
}

```

