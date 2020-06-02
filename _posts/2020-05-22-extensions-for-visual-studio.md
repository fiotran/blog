---
layout: post
title:  "Useful extensions for visual studio"
author: fiona
categories: [ Jekyll, tutorial ]
---
Here is my list some Visual studio extension I have come to know and love. It definitely speeds up my development time. I would avoid download any bulk standards as I find it does unexpected things and hinders more than aids my development.


#### Highlight typescript errors

Use TSLint. It is such a fantastic tool to highlight problems in your code.

````cd
ext install tslint
````

#### Format code

Use Prettier

````cd
ext install esbenp.prettier-vscode
````

#### Navigate between typescript | html | css in your project

Use angular2-switcher

- To go between typescript and html use `alt + o` or `shift + alt + o` on a mac
- To go between typescript and css use `alt + i` or `shift + alt + i` on a mac

To open side by side  in split view add the below the to settings.json
```typescript
"angular2-switcher.openSideBySide": true
```


#### Organise imports
If you are using TsLint you many have seen the error: 

> Import sources within a group must be alphabetized. (ordered-imports)tslint(1)

There are 2 ways to solve this:
- downloading the extension Typescript Heros
- or directly modifying the settings.json

```typescript
// In the vsc settings.json add the below
"editor.wordWrap": "bounded",
"editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "source.organizeImports": true
    }
```

Other settings I have found useful to implement for team commit consistency

```typescript
// In the vsc settings.json add the below
"html.format.wrapAttributes": "force-expand-multiline",
"javascript.preferences.quoteStyle": "single",
"javascript.preferences.importModuleSpecifier": "relative",
"prettier.configPath": "src/.vscode/.prettierrc" // if using Prettier
```


#### Auto generate snippets of code for speed in development

Angular Snippets 

````cd
ext install Angular2
````

Ones I freqently use are