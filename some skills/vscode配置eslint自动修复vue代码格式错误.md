### vscode如何配置eslint在Command+S时自动格式化代码
### vscode首先安装 eslint、vetur插件。
### 使用以下命令安装所需要的依赖
```
npm install --save-dev eslint-config-standard eslint-plugin-standard eslint-plugin-promise eslint-plugin-import eslint-plugin-node
```
### vscode中settings.json的配置
 ```
"eslint.enable": true,
"eslint.autoFixOnSave": true,
"eslint.run": "onType",
"eslint.options": {
     "extensions": [".js",".vue"]
},
"eslint.validate": [
    "javascript", "javascriptreact",
    {
        "language": "vue",
        "autoFix": true
    },
    {
        "language": "html",
        "autoFix": true
    }
]
 ```
 ### 在eslint的配置文件中添加standard配置，eslint的配置文件可以是.eslintrc.js或者是在package.json中的eslintconfig字段配置。
 ```
"extends": [
    "plugin:vue/essential",
    "standard"
]
 ```
 ### 配置好后应该就可以在保存时看到自动修复代码格式的相关操作了。