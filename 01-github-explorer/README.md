# Github Explorer&nbsp;&nbsp;<img src="https://cdn-icons-png.flaticon.com/512/1183/1183621.png" width="50" height="auto" align="center">&nbsp;&nbsp;<img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" width="50" height="auto" align="center">
### 🚀 - RocketSeat Ignite
Nesta sessão iramos adentrar um pouco mais no ecossistema React e entender como funciona o comando ```npx create-react-app <project-name>```, entenderemos toda a arquitetura de pastas de uma WebApp, para que no final de tudo isso, possemos implementar SPAs utilizando as melhores praticas do mercado e de forma fácil/limpa.

##### ⚙️ - Arquitetura do REACT
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

##### ❓ - Informações
> Nome: Matheus Ferreira Santos.
> Trilha: RocketSeat Ignite - Trilha REACT JS.
> Data: Quinta-Feira, 24 de agosto de 2023. 