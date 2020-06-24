# typescript
 <p>
    Dependencias usadas no projeto
    <ul>
    <li> <a href="https://www.npmjs.com/package/typescript"> typescript@2.3.2 --save-dev</a></li>
    </ul>
 </p>

 <p>
Pra rodar o typescript e necessário colocar a dependência typescript --save-dev. Apos colocar as dependências e necessário criar um aquivo json com as configurações baicas para o funcionamento e colocar também no packege.json
<br><br>
<h2>Configuração do tsconfig.json</h2>

```js
{
    "compilerOptions": {
        "target": "es6",
        "outDir": "app/js"
    },
    "include": [
        "app/ts/**/*"
    ]
}
```
<h2>Configuraçao do packege.json</h2>
<p>
No arquivo packet.json e necessário colocar o "compile": "tsc" para que o typescrip funcione corretamente.<br>Apos fazer as configurações necessárias e só rodar o comando no terminal npm run compile
</p>

```js
 "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "compile": "tsc"
  },
```
<p>

Quando terminar de rodar o comando, o arquivo app.ts gerado vai ocorrer um erro, pois o typescript precisa que as variáveis passada no construtor estejam como atributo na classe (como na estrutura das classes java e php). Declarando as variáveis antes do construtor vai corrigir o erro.
</p>

 ```ts
 class Negociacao
{
    _data;
    _quantidade;
    _valor;
    
    constructor(data, quantidade, valor)
    {
        this._data = data;
        this._quantidade = quantidade;
        this._valor = valor;
    }

    get data(){
       return this._data;
    }

    get quantidade(){
        return this._quantidade;
    }

    get valor(){
        return this._valor;
    }

    get volume(){
        return this._quantidade * this._valor;
    }
}
 ```
 </p>