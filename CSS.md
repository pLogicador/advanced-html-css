# 1. Herança e Cascata no CSS
### CSS é baseado em dois princípios: **cascata** e **herança**.

## **Cascata**
### O CSS aplica estilos com base em uma ordem específica chamada de "cascata", que envolve:

- **Especificidade**: Determinada pela importância dos seletores (elemento, classe, id, etc.).
- **Origem do estilo**: Pode ser definido pelo desenvolvedor (estilo embutido, CSS externo) ou pelo navegador (estilos padrão).
- **Ordem de precedência**: O estilo definido por último tem prioridade se houver conflito.

## Herança
### Herança significa que alguns elementos filhos herdam propriedades dos elementos pais, enquanto outras propriedades precisam ser explicitamente definidas.

Exemplos:

- Propriedades herdáveis: `color`, `font-family`, `line-height`, `visibility`.
- Propriedades não herdáveis (precisam ser aplicadas diretamente): `padding`, `margin`, `border`, `background`.

</br>
</br>

# 2. Valores de CSS: `inherit`, `initial`, `unset`, `revert`
Esses valores são usados para controlar a herança e o comportamento padrão de estilos.

### `inherit`: Faz o elemento herdar o valor de seu elemento pai.

````css

p.child {
  color: inherit; /* Herda a cor do pai */
}
````
### `initial`: Define o valor da propriedade para o valor padrão do CSS (como se o estilo não tivesse sido modificado).

````css
p.default {
  color: initial; /* Retorna ao valor padrão */
}
````
### `unset`: Reseta a propriedade. Se a propriedade for herdável, ela herda o valor do pai; se não for, retorna ao valor inicial.

````css
p.reset {
  color: unset; /* Herdável: herda, Não herdável: volta ao padrão */
}
````
### `revert`: Reverte para o estilo padrão do navegador ou para o estilo herdado da cascata.

````css
p.reverted {
  color: revert; /* Depende do estilo mais alto na cascata */
}
````
</br>
</br>

# 3. Sintaxe de Seletores no CSS
CSS oferece uma ampla variedade de seletores para estilizar elementos HTML com precisão.

## Seletores Básicos
- ### **Seletor de Tipo**: Seleciona todos os elementos de um tipo específico.

````css
p { color: blue; } /* Todos os <p> ficam azuis */
````
- ### **Seletor de Classe**: Seleciona elementos pela classe.

````css
.classe { color: green; } /* Todos os elementos com classe "classe" */
````
- ### **Seletor de ID**: Seleciona um elemento pelo ID.

````css
#id { color: red; } /* O elemento com id "id" */
````
## Seletores Combinadores
- ### **Descendente (` `)**: Seleciona todos os descendentes de um elemento pai.

````css
div p { color: purple; } /* Todos os <p> dentro de um <div> */
````
- ### **Filho Direto (`>`)**: Seleciona apenas o filho direto do elemento pai.

````css
div > p { color: brown; } /* Apenas <p> que são filhos diretos de <div> */
````
- ### **Adjacente (`+`)**: Seleciona o próximo elemento que está imediatamente após um elemento.

````css
h1 + p { color: orange; } /* O <p> logo após o <h1> */
````
- ### **Irmão Geral (`~`)**: Seleciona todos os irmãos seguintes de um elemento.

````css
h1 ~ p { color: yellow; } /* Todos os <p> após um <h1> */
````
## Seletores de Atributo
### Seleciona elementos com base nos atributos e valores:

````css
input[type="text"] { color: green; } /* <input> com type="text" */
````
## Seletores Pseudo-Classes
### Pseudo-classes aplicam estilos a estados específicos de um elemento, como `:hover`, `:focus`, ou `:first-child`.

````css
button:hover { color: red; } /* Quando o botão é "hovered" */
p:first-child { color: blue; } /* Primeiro filho dentro de seu pai */
````
## Seletores Pseudo-Elementos
### Pseudo-elementos selecionam uma parte específica de um elemento, como o primeiro caractere ou a primeira linha:

````css
p::first-line { color: gray; } /* A primeira linha do parágrafo */
````
</br>
</br>

# 4. Seletores Específicos: Classes e Hierarquia de Nomes
## CSS oferece várias formas de selecionar e combinar classes para criar hierarquias e controles de estilo complexos.

- ### **Classe com Hierarquia (`.`)**: Combina múltiplas classes aplicadas em um elemento.

````css
.pai.filho { color: blue; } /* Aplica-se quando ambas as classes estão em um elemento */
````
- ### **Classe Hierárquica Separada**: Quando as classes estão separadas, seleciona os elementos da classe filha que estão dentro do pai.

````css
.pai .filho { color: green; } /* Todos os .filho dentro do .pai */
````
</br>
</br>

# 5. Especificidade e Importância do CSS
## A especificidade define a prioridade dos seletores. A ordem de importância é:

### 1. Estilos inline (`style="..."` no HTML).
### 2. ID (`#id`).
### 3. Classes e pseudo-classes (`.classe`, `:hover`).
### 4. Seletores de tipo (`div`, `p`).

- ### `!important`: Força o estilo, sobrepondo todas as regras, exceto outras declarações `!important`.

````css
p { color: blue !important; }
````
</br>
</br>

# 6. Comentários no CSS
### Comentários ajudam a documentar o código, ignorados pelo navegador:

````css
/* Este é um comentário */
````
</br>
</br>

# 7. Modelo de Caixa e Box Model
## Cada elemento HTML é representado como uma caixa retangular que inclui:

- **Margin**: Espaço externo.
- **Border**: Borda ao redor.
- **Padding**: Espaço interno entre o conteúdo e a borda.
- **Content**: O conteúdo real, onde texto e imagens estão.
Controle do box model permite ajustar o layout de forma precisa.