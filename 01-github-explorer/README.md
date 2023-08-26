# Github Explorer&nbsp;&nbsp;<img src="https://cdn-icons-png.flaticon.com/512/1183/1183621.png" width="50" height="auto" align="center">&nbsp;&nbsp;<img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" width="50" height="auto" align="center">

### 🚀 - RocketSeat Ignite

Nesta sessão iramos adentrar um pouco mais no ecossistema React e entender como funciona o comando ```npx create-react-app <project-name>```, entenderemos toda a arquitetura de pastas de uma WebApp, para que no final de tudo isso, possemos implementar SPAs utilizando as melhores praticas do mercado e de forma fácil/limpa.

> OBS.: Nessa sequencia de estudos, estou utilizando o gerenciador de pacotes YARN, caso você não tenha ele instalado, rode o seguinte comando: ```npm install --global yarn``` para instar-lo globalmente em sua máquina, a grande maioria dos comandos eu informo o que usei, com yarn, e a sua possivel conversão para o npm, porém, não é sempre que eu lembro 🤡🤡🤡

<a name="navegação"></a>

###### Navegação:
É possivel que parte da nevagação ainda não esteja funcionando, porém, relevem.

- [Aula 01 - Arquitetura do REACT](#arquitetura)
- [Aula 02 - Babel](#babeljs)
- [Aula 03 - Webpack](#webpack)

<a name="arquitetura"></a>

##### ⚙️ - Arquitetura do REACT (Aula 01)

Para esse estudo, é de suma importancia entender a estrutura de cada comando e, obviamente, o que cada um deles fazem, dentro de seus respectivos contextos.

Até o momento, foi apresentado 3 comandos, que são eles:

- ```yarn init -y```
- ```yarn add react```
- ```yarn add react-dom```

A respeito do: **yarn init -y**, ou no npm: ```npm init -y``` esse comando é o **PONTAPÉ INICIAL DE TODA APLICAÇÃO QUE UTILIZA JAVASCRIPT**, utilizando esse comando você criará um arquivo: "package.json" que dentro dele irá conter todas as informações de seus projeto e, como ponto chave, salvará todas as informações de dependencias do projeto, funciona semelhantemente ao POM.XML do Java, onde é registrada todas as informações do projeto, como nome, pacote raiz, autor, dependencias e entre outras configurações.

> OBS.: Ao subir uma aplicação no GitHub, por padrão você deve ter o .gitignore para informar quais arquivos/pastas o Git deve ignorar, afinal, são arquivos desnecessários e que aumentam, drasticamente, o tamanho, em GBs, do repositório remoto. Você provavelmente irá se deparar, em repositorios onde o produto final está sendo implementado com tecnologias JavaScript, ou somente um produto dele (isso não importa), que, por exemplo, o diretório "node_modules" não irá entrar, ao se deparar com isso, clonando o repositorio em sua máquina, para que você possa instalar todas as dependencias que o projeto utiliza, e, consequentemente, conseguir utilizar o projeto localmente em seu computador, deve-se utilizar o comando ```yarn install``` ou ```npm install```, lembre-se de estar na pasta raiz do projeto, com esses comandos, seja la com qual gerenciador de dependencias você estiver utilizando, você será capaz de baixar todas as dependencias em seu computador e conseguirá utilizar o projeto e implementar novas features ou corrigir alguns bugs que você encontrou.

Avançando para o comando seguinte desse, encontramos: ```yarn add react```, ou caso utilize npm: ```npm install react```, se não me falha a memória, com esse comando você adicionará a dependencia do React no seu projeto, informando ao package JSON que você, em algum momento de sua aplicação, irá utilizar o React para desenvolver componentes e entre outros, **está basicamente informando que esse projeto irá utilizar o React**.

O último comando dessa lista é o: ```yarn add react-dom```, caso esteja usando npm será: ```npm install react-dom```, esse comando **informa para o seu projeto que você irá trabalhar com web**, esse DOM é justamente o Document do JavaScript, onde é possivel manipular o HTML, pegando elementos do próprio código HTML, e manipulando com o JavaScript/JQuery/Ajax e etc.

> OBS.: Como estamos desenvolvendo com REACT para WEB então se faz necessário baixar essa dependencia que citamos acima, porém, se estivesse criando a arquitetura do 0, como foi proposto nesse repositorio, e estivesse criando um projeto REACT para MOBILE, ao invés de baixar o yarn add react você substituiria por yarn add react-native, já que com React Native você é capaz de criar aplicações mobile fantásticas de forma muito eficiente e produtiva e com uma curva de aprendizado fantástica.

Até então é isso, essa foi a primeira aula da Trilha Ignite da RocketSeat onde, como principal objetivo, podemos análisar, de forma superficial, como funciona a arquitetura do REACT. Provavelmente em aulas futuras, ou até mesmo posterior a essa, continuaremos explorando essa arquitetura.

<a name="babeljs"></a>

##### 🌐 - Entendendo BABEL (Aula 02)

Essa aula tem como principal objetivo entender, e compreender realmente, como funciona o **babel** precisamos saber como isso aparece na Biblia. A torre de **babel** foi uma torre que o povo antigo tentou criar onde, resumidamente, eles acreditavam que se construissem uma torre muito alta, a ponto de passar das nuvens, eles conseguiriam chegar ao paraíso, porém, segundo a biblia, Deus separou o povo com linguas distintas para que essa construção não fosse concluida e é dai que vem o conceito de Babel do JavaScript.

###### 📖 - Conceito

O *babel* ele serve para **converter o nosso código para uma maneira que todos os navegadores/ambiente da aplicação consiga entender** todos os códigos escritos.

###### ❓ - Porque ele é necessário?

Pelo JavaScript ser uma linguagem que se atualiza constantemente, usando o próprio **REACT** como base, possa ser que, em alguma versão atual da biblioteca, existam maneiras de escrever o HTML dentro do código JS, por exemplo, de uma maneira que os navegadores ainda não entendem, **é ai que entra o babel!**

De acordo com esse cenário apresentado acima, o babel vai entrar em ação para converter esse código escrito para uma maneira que todos os navegadores mais modernos consigam entender, reduzindo assim (ou até mesmo acabando) com possiveis erro de compatibilidade, se é que eu posso dizer assim.

###### 📁 - Instalação

Para instalar o bebel em seu projeto, deve-se rodar o seguinte comando: ```yarn add @babel/core @babel/cli @babel/preset-env -D``` ou, caso esteja usando npm, deve-se utilizar: ```npm install @babel/core @babel/cli @babel/preset-env -D```.

> OBS.: A flag (bandeira) **-D** é utilizada para informar ao gerenciador de dependencias/pacotes que aquele(s) comando(s) irá(ão) ser instalado(s) como **dependencia de desenvolvimento**. O que isso significa? Significa que aquela dependencia não entrará em vigor quando o sistema subir para produção, a aplicação só irá precisar dele quando estiver no ambiente de desenvolvimento. 

A respeito dos comandos instalados, abaixo vai uma breve descrição de cada um deles, explicando o que eles representam:

- ```@babel/core```: É o coração do babel, sua biblioteca principal, básicamente 99% das funcionalidades do babel estão contidas dentro dela;
- ```@babel/cli```: É utilizada para o programador conseguir executar o babel atraves da linha de comando (caso queira testar, é possivel utilizar o comando ```yarn babel -h``` para abrir o menu de ajuda do babel no seu terminal **dentro do seu projeto, obviamente**)
- ```@babel/preset-env```: É uma biblioteca do babel que identifica qual ambiente a aplicação está sendo executada para converter o código da melhor maneira possivel.

> OBS.: Lembre-se de sempre que utilizar o babel criar o arquivo **babel.config.js** para que essa configuração realmente possa entrar em vigor.

###### 🧑‍💻 - Arquivo babel.config.js

Dentro do arquivo babel.config.js deve estar presente, pelo menos, o seguinte conteúdo:

~~~javascript
module.exports = {
    presets: [
        '@babel/preset-env'
    ]
};
~~~

Como explicado acima, o preset-env irá identificar em qual ambiente a nossa aplicação JavaScript está rodando e irá converter, da melhor forma possivel, o nosso código.

###### ❓ - É possivel converter algum código com babel para ver ele funcionando?

Sim! Isso é plenamente possivel, para converter um codigo JS com babel é possivel da seguinte maneira:

1. Crie um diretório *./src* em seu projeto, **caso ele não exista**;
2. Adicione um arquivo *index.js* (ou qualquer outro nome de sua preferencia) e salve-o;
3. Abra o terminal e digite o seguinte comando: ```yarn babel ./src/index.js --out-file dist/bundle.js```;
4. Seja feliz!

> Destrinchando o código de "compilação" do babel: o comando inicial, obviamente, chamando o babel: "yarn babel ..." e passando logo após isso o caminho do arquivo que você, programador, quer compilar, no meu caso "./src/index.js", o comando inteiro ficou, até o momento: "yarn babel ./src/index.js". Logo após isso, informeu a flag "--out-file", que poderia ser minimizada para -o, e em sequencia o diretório de onde quero guardar o arquivo compilado, passando também o seu futuro nome: "./dist/bundle.js", **bundle.js** é uma convenção utilizada entre os desenvolvedores para códigos que foram gerados a partir do babel, e **dist** está informando que é a pasta de distribuição, obviamente é so uma sigla do inglês. O codigo final é: "yarn babel ./src/index --out-file ./dist/bundle.js"

Caso você tenha o minimo de conhecimento em React, irá vir a seguinte pergunta em sua mente: *"Se eu posso transformar códigos JavaScript atuais para versões mais padronizados que o navegador possa entender, o que será que iria acontecer se eu simplesmente criasse um componente e pedisse para ele rodar?"*

E provavelmente você iria atualizar o arquivo index.js para algo mais ou menos assim:

~~~javascript
import React from "react";

const helloComponent = () => {
    return <>Hello world!<>
};
~~~

e quando você rodasse o comando: ```yarn babel ./src/index.js --out-file ./dist/bundle.js``` iria, exatamente, dar uma exception!

Kkkkkk, exatamente, uma exception, e é ai que sua mente buga: *"Se o babel serve para interpretar códigos javascript, atuais, em códigos javascript que todos os navegadores entender, porque eu não consigo "compilar" um código React, que é bastante atual, em um código que qualquer navegador entenda? **Propaganda enganosa?**"*

Ele até consegue fazer isso, porém, quando estavamos baixando todas as dependencias do babel não baixamos também uma dependencia para fazer com que ele compile codigos React.js, então ele irá tentar compilar com o preset-env padrão que baixamos e não irá ter sucesso. Para conseguir obter êxito na conversão de arquivos React com o babel, deve-se instalar o seguinte comando: ```yarn add @babel/preset-react -D```, não preciso explicar o que ele faz, certo?

> Para desencargo de consciencia: **yarn add** irá adicionar algum pacote em seu projeto, no nosso caso o pacote **@babel/preset-react** que servirá para compilar arquivos React e transformar-los em código *JavaScript* e a flag **-D** é para indicar, como já falado, que é uma dependencia de desenvolvimento.

Após instalar essa dependencia nova no projeto, se faz necessário informar, no arquivo **babel.config.js** que é para ele utilizar esse preset novo, então para isso, altere o arquivo **babel.config.js** para o abaixo:

~~~javascript
module.exports = {
    presets: [
        '@babel/preset-env',
        '@babel/preset-react'
    ]
};
~~~

E pronto! Ao tentar rodar o index.js ele já estará convertendo e retornando algo mais ou menos assim:

~~~javascript
"use strict";

var _react = _interopRequireDefault(require("react"));

function _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { "default": obj }; }

var app = function app() {
  return /*#__PURE__*/_react["default"].createElement(_react["default"].Fragment, null, "Hello world!");
};
~~~

**????????????????????????????????, Uma loucura do C@#$&ho!!!**
Não vá esperando que eu adicione o que esse código está fazendo linha por linha, eu só sei que no final irá aparecer o Hello World na tela igual fizemos no componente KKKK, porém, por mais que esse código fique bastante extenso tem coisas piores por vir!

##### 🌎📦 - Entendendo Webpack (Aula 03)

Dentro de sua aplicação, no código JavaScript, atualmente, você pode importar outros arquivos JS dentro dele, mas com React, ou em outras libs, você não irá importar somente arquivos JS, obviamente, você acaba tendo a necessidade de importar arquivos SCSS, CSS, Imagem (png, jpg, svg) e entre outros arquivos (qualquer tipo de arquivo literalmente), e o ***webpack*** vai basicamente definir algumas configurações, que chamamos de ***LOADERS***, que *vai ensinar a aplicação como ele deve tratar cada tipo de arquivo importado e ele irá pegar cada tipo desses arquivos e irá converter para um padrão que os browsers entendem*. **O webpack trabalha semelhantemente ao babel**.

> Resumidamente: O Babel e o webpack irão trabalhar em conjunto para fazer garantir que sua aplicação seja entendida por todos os navegadores!

###### 📁 - Instalação

Para instalar o ***webpack*** em seu projeto, deve-se rodar o seguinte comando: ```yarn add webpack webpack-cli babel-loader -D``` ou, caso esteja usando npm, deve-se utilizar: ```npm install webpack webpack-cli babel-loader -D```.

E assim como o babel, deve-se criar um arquivo, no root do projeto, com o nome: **webpack.config.js**

Dentro dele você irá definir algumas configurações obviamente, e no fim, ele irá ficar mais ou menos assim:

~~~ javascript
const path = require('path');

module.exports = {
    entry: path.resolve(__dirname, 'src', 'index.jsx'),
    output: {
        path: path.resolve(__dirname, 'dist'),
        filename: 'bundle.js'
    },
    resolve: {
        extensions: ['.js', '.jsx'],
    },
    module: {
        rules: [
            {
                test: /\.jsx$/,
                exclude: /node_modules/,
                use: 'babel-loader'
            }
        ],
    }
};
~~~

> Destrinchando o código: Na primeira linha ***se faz necessário importar o 'path' para que,*** a partir do seu sistema operacional, ***o JavaScript possa trabalhar com os diretorios da maneira correta.***

> Seguindo mais um pouco, exporto um modulo que de cara ***defino um entrypoint***, dentro desse entrypoint é necessiário informar qual é o arquivo inicial da aplicação, '__dirname' *(para informar que, é a partir do diretorio desse arquivo que ele deve acionar os proximos diretorios)*, 'src' *(para informar que deve entrar em src)* e 'index.jsx' *(para informar que esse é o arquivo procurado).*

> Abaixo dele tem a propriedade ***output***, que, como o nome ja diz, informa qual será o caminho e o nome do arquivo, quando ele for "compilado".

> Na sequencia temos o ***resolve*** que informamos dentro de *"extensions"* quais arquivos o webapp pode ler, por padrão é somente ".js", porém, vamos informar que ele pode ler também ".jsx" (ou um ou outro). 

> Depois deve-se informar um ***module***, e dentro dele nós configuramos justamente como a aplicação deve se comportar quando estiversos importando cada um dos tipos de arquivos citados anteriormente *(.css, .jpg, .scss, .svg e etc)*, definimos uma propriedade rules (um array de regras) e definimos um objeto, no código acima defino somente a regra para arquivos que terminam com ".jsx". Dentro da propriedade *"test"* definimos uma expressão regular (regex) para verificar se o arquivo é um arquivo javascript ou não, basicamente ele só ira verificar a extensão dele, o que vem depois do ".", exemplo: "blabla.img" não é javascript, porém, "blabla.jsx" é. Na linha seguinte, com o *exclude*, informo que **DEVE SER EXCLUIDO (ou ignorado) TODA A PASTA NODE MODULES** e logo após informo que ele deve usar o babel-loader (que é a integração do webpack co o babel), e ele basicamente faz o seguinte: Ao tentar importar um arquivo .jsx ele chama o babel-loader e converte esse arquivo ".jsx" para ".js" e joga la no .dist/bundle.js.

Para testar todas essas configs acima, você pode criar um arquivo: App.jsx dentro do diretório *./src* com qualquer código, o meu está assim:

~~~ javascript
import React from "react";

export function App() {
    return <h1>Hello world!</h1>
}
~~~

e dentro do index.jsx (o meu arquivo principal configurado no webpack) eu tenho:

~~~ javascript
import React from "react";
import { App } from "./App";
~~~

ao rodar o comando: ```yarn webpack```, ou ```npm webpack``` *(ACREDITO QUE SEJA ESSE, POSSO ESTAR ERRADO)*, no terminal ele gerará a pasta ./dist com o arquivo index.jsx "compilado", dentro dele o código ficará assim:

~~~ javascript
/*! For license information please see bundle.js.LICENSE.txt */
(()=>{"use strict";var t={408:(t,e)=>{Symbol.for("react.element"),Symbol.for("react.portal"),Symbol.for("react.fragment"),Symbol.for("react.strict_mode"),Symbol.for("react.profiler"),Symbol.for("react.provider"),Symbol.for("react.context"),Symbol.for("react.forward_ref"),Symbol.for("react.suspense"),Symbol.for("react.memo"),Symbol.for("react.lazy"),Symbol.iterator;var o={isMounted:function(){return!1},enqueueForceUpdate:function(){},enqueueReplaceState:function(){},enqueueSetState:function(){}},r=Object.assign,a={};function n(t,e,r){this.props=t,this.context=e,this.refs=a,this.updater=r||o}function c(){}function p(t,e,r){this.props=t,this.context=e,this.refs=a,this.updater=r||o}n.prototype.isReactComponent={},n.prototype.setState=function(t,e){if("object"!=typeof t&&"function"!=typeof t&&null!=t)throw Error("setState(...): takes an object of state variables to update or a function which returns an object of state variables.");this.updater.enqueueSetState(this,t,e,"setState")},n.prototype.forceUpdate=function(t){this.updater.enqueueForceUpdate(this,t,"forceUpdate")},c.prototype=n.prototype;var s=p.prototype=new c;s.constructor=p,r(s,n.prototype),s.isPureReactComponent=!0;Array.isArray,Object.prototype.hasOwnProperty},294:(t,e,o)=>{o(408)}},e={};!function o(r){var a=e[r];if(void 0!==a)return a.exports;var n=e[r]={exports:{}};return t[r](n,n.exports,o),n.exports}(294)})();
~~~

**????????????????????????????????, Uma loucura do C@#$&ho novamente!!!**

Esse é simplesmente impossivel de saber o que está fazendo ASHUASHUA, porém, boas noticias, **o webpack já está funcionando e está integrado com o babel!**

> OBS.: O comando ```yarn webpack```, ou ```npm webpack```, pode gerar alguns alertas, mas, isso não é muito relevante e pode ser ignorado

[Voltar para a sessão de navegação.](#navegação)

##### ❓ - Informações
> Nome: Matheus Ferreira Santos.
> Trilha: RocketSeat Ignite - Trilha REACT JS.
> Data Inicial: Quinta-Feira, 24 de agosto de 2023. 