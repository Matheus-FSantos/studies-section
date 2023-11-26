# Estágio Desenvolvedor - Real Seguro Viagem

### ❓ - Contexto

Olá, se você entrou nesse repositório então é porque ficou curioso para saber minha resposta completa para as questões apresentadas.

A plataforma do Google Forms não me permitiu escrever a minha resposta completa para cada pergunta apresentada, porém so fui saber ao tentar submitar o teste, então, decidi vir no meu repositorio criar um README.md para enviar as minhas reais respostas para cada questão e não sua "versão simplificada".

#
### 📚 - Questões

#### **1** **) Qual a diferença entre programação funcional e orientada a objetos?**

**R:** A programação orientada a objetos e a funcional são dois paradigmas de programação bem famosos e comuns em linguagens, ambos são base para linguagens como: Java, Lua, Python, JavaScript e etc.

Quando falamos de programação orientada a objetos, ela veio para organizar o código que, nós, desenvolvedores fazemos, tornando eles mais tranquilo de dar manutenção, e está mais voltado para a programação girando em torno de objetos (que são instancias de classes), é comum ver pessoas falando que a orientação a objetos resolve problemas relacionado a duplicidade de códigos, o que realmente é uma verdade, é possivel fazer um código muito enxugado usando todos os 4 pilares que esse paradigma oferece (abstração, encapsulamento, herança e polimorfismo). Resumidamente, a Orientação a Objetos tem como fundamento representar o mundo real no código (o que eu discordo, acredito que ela visa representar as regras de negócio da sua aplicação, da maneira mais limpa possivel,  dentro do mundo da programação, não necessáriamente o mundo real, isso varia de regra de negócio para regra de negócio).

Já na programação funcional, ela não gira em torno de instancias de classes (os famosos objetos) ela gira em torno de funções de primeira-classe ou seja, elas podem ser passadas como parametro para outras funções e até mesmo como retorno de outras funções (as famosas funções de alta ordem), podem ser chamadas dentro de outras funções e afins,

resumidamente, a programação orientada a objetos, como falado anteriormente, é voltada para a instancia de classes e a programação funcional é voltado para as funções e suas operações.

Ficou meio grande kkkk, mas são conceitos muito bacanas de trabalhar e de debater. Graças a um grande professor amigo meu, consigo hoje debater e rever conceitos voltando mais para o lado filosofico, não que eu fui um platão da vida kkkk, mas é muito legal, eu tenho um repositorio voltado para estudos, caso tenha um tempo, de uma olhadinha lá em algumas anotações que faço, até então só tem um conteudo de React: https://github.com/Matheus-FSantos/rocketseat-ignite/tree/main/01-github-explorer e um conteudo de Java EE: https://github.com/Matheus-FSantos/4log-products.

#

#### **2** **) Pode explicar 3 design patterns?**

**R:** Os design patterns, como eu gosto de dizer, são meios de, nós, programadores escrevermos códigos mais sustentáveis e manuteníveis, com eles são possiveis obter:

1. Escalabilidade;
2. Padronização;
3. Legibilidade de código.
e entre outros que não me lembro agora kkkkk.

3 design patterns, muito conhecidos são:

1. Singleton Pattern - que diz, resumidamente, que uma classe tenha apenas uma instancia e que ela tenha um ponto global de acesso;

2. Observer Pattern - é um padrão que tenta definir uma dependencia um para muitos entre objetos, e quando um muda o estado os outros são atualizados automaticamente (é um padrão muito famoso, e o Programador e youtuber felipe dechamps, dono do tabnews, fez um video sobre um jogo online que ele estava desenvolvendo com a comunidade que fazia uso desse padrão, bem bacaninha);

3. Strategy Pattern - ele basicamente visa definir uma familia de algoritmos que no final pode ser trocado por outro sem fazer a menor diferença, resumidamente, o cliente escolhe o algoritmo que irá utilizar, tipo em um sistema de transação financeira, que tu pode escolher entre pagar com paypal, com picpay, no debito, no cartão, etc.

#
### **3** **) Em Javascript, '1' é igual a 1?**

**R:** Essa é uma pergunta complexa KKKK, porém, a melhor resposta é: depende.

Analisando essa pergunta com o conceito de programação fortemente tipada, a resposta seria "não" de cara, afinal, um caractere ('s', '1', objetos envolvidos por uma aspas simples) não é igual ao um valor numerico inteiro (1, 2, 3, 4, 10000).

Porém, nós sabemos que a linguagem javascript não é fortemente tipada, como C#, Java, C, Swift, Kotlin e entre outros, ela é uma linguagem fracamente tipada, como PHP e Python, então dentro dela tudo é resumido por: Strings (palavras envolvidas por aspas simples e duplas), valores numericos (com pontos flutuantes ou não), valores booleanos (verdadeiro ou falso) e alguns outros que não vem ao caso nesse momento.

Sabendo que javascript utiliza esses 3 tipos primitivos como base de todos os sistemas, ao se comparar "1" ('1') com 1 utilizando o operador padrão de igualdade (==), como no exemplo abaixo:

~~~ javascript
console.log('1' == 1);
~~~

o retorno seria "true", porque? ao se comparar com (==) o javascript entende que você está querendo comparar o conteudo das variáveis, logo, 1 é igual a '1', eles tem o mesmo conteudo, agora se comparar com o operador de igualdade estrita (===) como no exemplo abaixo:

~~~ javascript
console.log(1 === "1"); /* veja que nesse usei aspas duplas para mostrar que tanto faz */
~~~

o resultado seria "false", porque? porque agora sim ele está usando conceito das linguagens fortemente tipadas, comparando os tipos delas, que são passados dinamicamente em tempo de execução, e se perguntando: "pô, String é igual a Number? acho que não, retorna um false ai para ele". Enfim, javascript é uma linguagem muito boa de se trabalhar, e por mais que todos falem: "Eu gosto de javascript porq é uma linguagem fácil" para mim é uma grande mentira, javascript é uma linguagem tão complexa quanto Java,  porém, a complexidade está alocada em lugares diferentes kkkk.

#
#### **4** **) Escreva uma função para retornar se um número é par ou ímpar (na sua linguagem de preferência).**

**R:** em Java, uma função que retorna se o numero é impar ou é par pode ser escrita e chamada assim:

~~~ java
public class Sum {
  private static String typeOfNumber(Double number){
    Integer result = (number %2);
    return (result == 1) ? "Impar" : "Par";
  }

  public static void main(String[] banana) {
    System.out.println(typeOfNumber(2)); /* Par */
    System.out.println(typeOfNumber(1)); /* Impar */
    System.out.println(typeOfNumber(10)); /* Par */
  }
}
~~~

é possivel reduzir mais ainda o código da função colocando a expressão da variável result dentro do operador ternário, porém, por ser uma função simples, isso é opcional.

#
#### **5** **) Escreva em sua linguagem favorita uma forma de validar a seguinte demanda: Verificar se a palavra "olá" está contida na frase "olá joão".**

**R:** em Java você pode fazer:

~~~ java
public class StringManipulation {
  public static void main(String[] args) {
    String word = "olá";
    System.out.print(new String("olá joão").contains(word));
  }
}
~~~

em javascript a ideia é a mesma:

~~~ javascript
function wordContains(word) {
  const fullWord = '"olá joão";
  return fullWord.includes(word) ? "contem" : "não contem";
}

console.log(wordContains("olá")); /* contem */
console.log(wordContains("joão")); /* contem */
console.log(wordContains("teste")); /* não contém */
~~~

#
#### **6** **) Você está familiarizado com sistemas de versionamento de código, como o Git? Se sim, cite ao menos três comandos.**

**R:** git add "file name" (ele irá adicionar "informar" ao git que o arquivo que você passou será adicionado ao proximo commit);

seguindo a mesma linha temos o: git commit -m "message", exemplo: git commit -m "feat: add new admin route", esse comando serve para informar adicionar um novo commit para os arquivos você rastreou com o comando anterior;

git branch -M "branch name or new branch name", esse comando server para te mover para uma branch, caso ela não exista, ela cria uma com o nome que você informou e te move para ela;

git status -s, esse comando serve para te informar qual é a situação do seu repositorio local, os arquivos rastreados e os não rastreados;

git pull, esse comando serve para atualizar o seu repositorio local com o repositorio remoto;

git push -u origin "branch name", esse comando serve para adicionar os arquivos commitados para o respositório remoto (o -u origin "branch name", faz com que, quando você estiver nessa branch novamente, possa dar os comandos simplificados: git pull e push);

git log --oneline, esse comando mostra todas os commits realizadas naquela branch local/remoto que você se encontra, usando a flag --oneline ele irá encurtar a lista, deixando somente a versão simples do ID do commit e sua respectiva mensagem, exemplo: "d4ca1a9 chore: update README.md".

enfim, existem varios outros kkkk, git é uma tecnologia fantastica que nos ajuda muito no dia a dia, um curso muito bom que me fez aprender e entender como funciona a ferramenta Git, por baixo dos panos, é o curso da Atlassian, dona do Jira e BitBucket, segue o link para conferir:

https://www.coursera.org/learn/version-control-with-git

#
#### **7** **) Qual a diferença de um merge e um rebase?**

**R:** o merge basicamente realiza a união entre duas branchs, exemplo:

tenho uma branch "backend", e desejo corrigir um bug em cima dessa branch "backend", então eu crio uma branch nova, exemplo: "backend-bug-solution", realizo todas as atualizações necessárias e depois faço um merge da branch "backend-bug-solution" para a branch "backend" e ela agora conterá as alterações que você realizou na ramificação "backend-bug-solution".

agora, o rebase ele atualiza uma branch com as alterações realizadas em uma outra branch, exemplo: 

enquanto você estava realizando as devidas manutenções na ramificação "backend" (dentro da branch "backend-bug-solution") outro dev estava alterando a branch "backend" e subiu alguns commits novos, então quando você for mergiar a branch "backend-bug-solution" para a "backend" provavelmente irá dar conflito de versões, o git rebase entra para resolver esses conflitos de versões (se não me engano ele se guia pelas datas e horas dos commits e vai atualizando tudo certinho).

#
#### **8** **) Qual a diferença de posição fixa e absoluta?**

**R:** OBS.: Assuma que está em uma tela branca com uma div quadrada azul (que chamarei de "componente")

Bom, em CSS existem alguns tipos de posicionamentos, eles são:

Posicionamento Relativo: Essa propriedade NÃO altera o fluxo do "componente" no layout do sistema, caso você queira trabalhar com ela, irá trabalhar com base no posicionamento atual dele no sistema, exemplo, você aplicou as seguintes propriedades no "componente" (explicado em OBS):

~~~ CSS
.componente {
  position: relative;
  right: 0.9rem;
}
~~~

iremos supor que o "componente" está localizado no px 100 da sua tela, o código acima, com base no px 100, irá deslocar o seu "componente" 0.9 rem  a esquerda (afinal, usa-se a propriedade right para afastar da direita e propriedade left para afastar da esquerda) o que da (através do site conversor HASUDAUAHSDUA) um valor aproximado a 14.4 px e se usarmos a matemática a nosso favor:

x = 100px - 14.4px
x = 85.6px (nova posição do "componente" na tela).


Entendendo como esse posicionamento funciona, eu posso explicar como os outros funcionam, ambos funcionam de formas semelhantes, ou seja, ambos alteram o fluxo padrão do "componente" quando é utilizado, porém, com uma peculiaridade:

Position Absolute: é possivel controlar até onde ele ficará contido, exemplo, se tivermos um "container-pai" para o "componente" podemos fazer o seguinte:

~~~ CSS
.container-pai {
  position: relative;
}

.container-pai .componente {
  position: absolute;
  top: 0px;
  left: 0px
}
~~~

assim eu limito onde o "componente" irá ficar, ou seja, ele irá ficar preso no canto superior esquerdo do "container-pai" porém ele ficará totalmente fora do layout padrão desse componente, o que, poderia nos dar possibilidades de design interessantes, se for devidamente trabalhado por um profissional.

agora quando estamos trabalhando com posicionamento fixo a coisa não funciona dessa forma, afinal, NÃO EXISTE MANEIRA DE SEGURAR ELE, ele simplesmente manda nele mesmo, ele fica com a posição em relação a tela do usuário, exemplo, se você colocar a seguinte propriedade no "componente":

~~~ CSS
.componente {
  position: fixed;
  bottom: 10px;
  right: 10px;
}
~~~

ele SEMPRE ficará no canto inferior direito da tela do usuário, mesmo ele rolando a tela para cima e para baixo, e não existe maneira, e nem truque, para manter ele fixo, nem usando o "hackzinho" acima, do "container-pai" com posicionamento relativo.

Eu utilizei esse conceitos em um projeto clone do discord que fiz como atividade na minha faculdade, um projeto que basicamente utilizou conceitos de flex-box, posicionamento, até tive que corrigir uns bugs que apareceram na versão oficial do discord kkk, foi bem bacana, segue o link:

https://matheus-fsantos.github.io/clone-dscord/src/pages

E também tenho algumas anotações que fiz em sala de aula sobre esse conteudo:

https://github.com/Matheus-FSantos/studies-section/tree/main/04%20-%20Posicionamento%20e%20SASS

#
#### **9** **) Comente um desafio de programação que você fez e gostou de ter realizado. Por que?**

**R:** Em uns tempos atrás realizei um teste tecnico para uma vaga de Desenvolvedor Estagiário Java e o escopo do teste era: ler um arquivo .pdf extrair determinadas infos e retornar, via console, o que foi recebido, de acordo com os inputs do usuário, obviamente não fiz somente isso porque um bom profissional não faz apenas o que lhe foi passado, faz a mais do que é o esperado.

Achei bastante curioso, porque atualmente a maioria da galera somente passa CRUD de heroi, CRUD de não sei que lá e se passar está aprovado se não conseguir fazer reprovou, gostei pois eles inovaram, me fizeram sair da minha zona de conforto e pesquisar um pouco mais sobre uma biblioteca nova, que eu nunca  tinha usado, e como funcionava a leitura de arquivos .pdf com Java, para esse teste usei uma lib chamada: Apache PDFBox, enfim, resultado: sistema realizado, teste entregue e uma reprovação da empresa, não os culpo, poderia ter ficado um pouco atento no ponto que me faltou: Testes Unitários, porém, me ensinou a sempre ir preparado para qualquer teste que fizer, pois eu não sei o que será passado e mesmo tendo conhecimento teorico e prático o mercado pode nos pregar uma peça e passar a perna em qualquer um.

A solução desse teste foi upada em meu GitHub (como pedido da empresa) e caso queiram dar uma olhada desenvolvi uma documentação escrita do projeto realizado:

https://github.com/Matheus-FSantos/vc-x-solutions/blob/main/Documenta%C3%A7%C3%A3o/Documenta%C3%A7%C3%A3o.pdf 

## FIM 🥳🎉🎉