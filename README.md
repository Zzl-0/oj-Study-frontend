# oj-Study-frontend

# Windows 拉取前端代码报错，LF 和 CRLF 冲突
```
git config --global core.autocrlf false
```

# 开发环境
```
node.js  V 18.18.0  (18 或者 16 版本都行)
npm 9.5.1
```

## 工程化配置，vue 脚手架自动配置了代码美化，使用 webStrom 开发的话需要开启美化插件，vscode 请自行查询
```
在setting 中找到 prettier, prettier package 选择 node_Modules\prettier
开启 C + Alt + L 的全局格式化配置，就可以使用了。
```

## 引入的组件库
```
npm install --save-dev @arco-design/web-vue

请求工具类
npm install axios

根据后端接口文档自动生成请求代码工具
npm install openapi-typescript-codegen --save-dev

MD 编辑器
npm i @bytemd/vue-next
npm i @bytemd/plugin-highlight @bytemd/plugin-gfm

代码编辑器
npm install monaco-editor

vue-cli 项目整合 monaco-editor
npm install monaco-editor-webpack-plugin
```

## 根据后台生成代码

```shell
openapi --input http://localhost:8121/api/v2/api-docs --output ./generated --client axios

记得改一下 openapi 中 CREDENTIALS 的参数为 true ，位置在 "/generated/core/OpenAPI
```


## Project setup

```
yarn install  or  npm install  
```

### Compiles and hot-reloads for development

```
yarn serve
```

### Compiles and minifies for production

```
yarn build
```

### Lints and fixes files

```
yarn lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
