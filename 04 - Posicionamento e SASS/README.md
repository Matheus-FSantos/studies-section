# Aula 02 - Desenvolvimento Web TADS

### Posicionamentos no CSS

no CSS existem 3 tipos de posicionamento, eles são: relativo, absoluto e fixado, em resumo, eles funcionam da seguinte maneira:

- **Position Relative**: básicamente, dispõe o item na tela para que ele fique "flutuando", porém, seguindo o seu flow (posição inicial).
Position -> left, right, top, bottom -> trabalham com os pixeis de acordo com a posição natural dele, por ex: se tiver left: 10px, ele irá adicionar 10px a esquerda da sua posição natural.


- **Position Absolute**: não faz mais parte do flow do layout, ele fica flutuando a partir de qualquer lugar.
quando se usa posição absoluta é necessário informar para o css que o seu pai (div que engloba o item absolute) é relativo, para que o item absoluto fique flutuando somente dentro do seu "container" direito.

- **Position Fixed**: ele também sai do flow, porém, não é possivel englobar ele dentro de um pai, como o absolute.
OBS.: Se rolar o scroll para baixo, ele não sai da posição informada, sempre se mantém no mesmo lugar.


### SASS
Com o sass você deixa a escrita do seu CSS mais clean, no caso, ele é um "framework" de CSS, onde, no final das contas, os arquivos .sass/.scss são .css

# Variaveis
para criar uma variavel em SASS é necessiario: adicionar **"$<var_name>: value;"**

example: **$white: #fff;**

# Componentes
para criar componentes em sass é necessário informar para o compilador que o arquivo informado não sera "compilado", para que isso se transforme uma realidade é necessário adicionar "_" antes do nome, ou seja, se o seu arquivo é "nome.scss" e deseja transformar-lo em componente, para importar futuramente, deve-se transformar de "nome.scss" para "_nome.scss"

# Imports
para poder importar o componente sass, é necessiário utilizar o decorator **"@import <file_location>;"**

exemplo: **@import "../../blabla/component.scss";**
