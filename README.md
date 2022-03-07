# Creación de proyecto nuevo de TypeScript en Visual Studio Code

Crea el directorio del proyecto
`npm init`
`npm install typescript --save-dev`

En la sección scripts de package.json:

```json
{
"tsc" : "tsc",
"tsc:w": "tsc --watch",
"http-server": "npx http-server ./ -o"
}

```
`npm run tsc -- --init`

Personaliza tsconfig.json
```json
{
  “compilerOptions:”: {
    “target”: “es2017”,
    “module”: “es2020”,
    “sourceMap”: true,
    “outDir”: “./dist”,
    “esModuleInterop”: true,
    “forConsistentCastingInFile”: true,
    “strict”: true,
    “skipLibCheck”: true
  }
}

```

Implementa los siguientes elementos en ./src/index.html


Implementa la siguiente función de TypeScript en ./src/main.ts
```html
    Result is: <span id="output"></span>
    <script src="../dist/main.js"></script>
    <script>
        const result = add(40, 50);
        document.querySelector('#output').innerHTML = result;
    </script>
```

```ts
function add(x:number, y:number) : number {
    return x + y;
}
```

`npm run tsc` o 

`npm http-server`

