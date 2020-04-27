# Webpack-React
Repositório com configurações base para servidor de desenvolvimento ReactJS
## Prompt
Iniciar o servidor com **NPM Start** no prompt
## Porta Local
para alterar a porta do servidor local
deve ser alterado nos arquivos
### webpack.config.js
`module.exports = {
    devtool: 'sorce-map',
    entry: [
        'react-hot-loader/patch',
        'webpack-dev-server/client?http://localhost:3000',
        'webpack/hot/only-dev-server',
        path.join(__dirname,'src', 'index')
    ],`

**altere a porta na propriedade entry**
#### Server.js

`.listen(3000,(err) =>{
    if(err){
        return console.log(err);
    }
    console.log('Listening on http://localhost:3000');
} )`

**Altere o primeiro parametro de listen**





## Modulo 1 - Parte 2

### Aula M1#A07 - Props

Para passar props devemos utilizar uma sintaxe parecida com as propriedades do HTML quando instanciarmos nosso componente exemplo:
 `<Title name='Wellington de Andrade' />` 
 
 para pegarmos as props usando JSX no arquivo do componente devemos usar **{this.props.NOME_DA_PROP }** na função render exemplo:
 `<div>Olá {this.props.name} </div> `
 


### Aula M1#A08 - Atributos HTML

Algumas propriedades do html tem a mesma sintaxe de palavras reservadas do JS, por isso tem uma forma diferente em JSX como por exemplo o class e o for.

No JSX se usa className e htmlFor respectivamente para esses casos.

#### HTML
`<div ***class***="container"></div>`
`<label ***for**="User>Label</label>`
`<input id='User' type="text">` 

#### JSX (REACT)
`<div ***className***="container"></div>`
`<label ***htmlFor**="User>Label</label>`
`<input id='User' type="text">`


### Aula M1#A09 - getDefaultProps

Caso a propriedade não seja passada no momento da renderização do componente pode ser utilizada a  função getDefaultProps para definir valores padrões para esses casos exemplo:

` getDefaultProps: function () {
    return {
      name: 'Desconhecido'
    }
  },`
 
Após o **createClass**.



### Aula M1#A10 - Outros tipos de dados via props

Para passar outros tipos de dados (!string) devemos utilizar as **{}** por exemplo:

`<Title idade ={18}/>`


