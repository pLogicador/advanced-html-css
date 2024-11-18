# O Que é HTML?
**HTML** (HyperText Markup Language) é a linguagem de marcação padrão utilizada para criar e estruturar o conteúdo na web. Diferente das linguagens de programação tradicionais, HTML não é utilizado para realizar cálculos ou manipulações complexas; em vez disso, ele **organiza e define a estrutura do conteúdo** de uma página. Um arquivo HTML é basicamente um arquivo de texto que contém uma série de **tags** ou **elementos** que definem o que cada parte do conteúdo representa.

## Estrutura do HTML: A Base do Desenvolvimento Web
Quando falamos em desenvolvimento frontend, o HTML é a fundação de toda página web, formando a base da chamada "pirâmide" do frontend:

1. **HTML** - A fundação e estrutura de uma página web.
2. **CSS** - A camada que define o estilo visual, ou seja, a aparência.
3. **JavaScript** - A camada de comportamento, responsável pela interatividade.

Cada camada dessa pirâmide trabalha em conjunto para formar uma página web completa e funcional: o HTML estrutura o conteúdo, o CSS estiliza, e o JavaScript adiciona funcionalidades dinâmicas.

## Estrutura e Marcação
Dentro do HTML, cada elemento possui um papel específico que vai além de apenas exibir texto ou imagens; ele define a semântica do conteúdo. Por exemplo:

- A tag `<header>` define o cabeçalho de uma página ou de uma seção, enquanto a <footer> representa o rodapé.
- A `<nav>` identifica uma seção de navegação.
- A `<article>` indica um conteúdo independente e auto-suficiente.
- A `<section>` agrupa seções temáticas.

Esses elementos são chamados de **elementos semânticos**, pois dizem ao navegador (e ao desenvolvedor) qual é o propósito do conteúdo dentro da página. Esse foco na semântica torna o HTML mais acessível e ajuda buscadores e navegadores a interpretarem melhor o conteúdo, o que também contribui para uma boa otimização para motores de busca (SEO).

## O Papel da Semântica no HTML
A "família" dos elementos semânticos do HTML foi criada para fornecer significado ao conteúdo. Quando você escolhe a tag correta, não está apenas definindo o estilo visual, mas o significado e a função daquela parte do conteúdo.

Essa estrutura semântica torna a página mais intuitiva para qualquer pessoa ou tecnologia (como leitores de tela ou robôs de busca) entenderem o conteúdo e navegarem por ele. A escolha dos elementos certos ajuda a melhorar a experiência de acessibilidade para pessoas com deficiência e facilita o trabalho de indexação dos motores de busca.

## HTML, CSS e JavaScript: Uma Combinação Poderosa
O HTML forma a base de tudo na web, mas ele não trabalha sozinho. Para criar experiências completas e dinâmicas, ele trabalha em conjunto com:

- **CSS** (Cascading Style Sheets): Controla a aparência da página, definindo cores, fontes, layouts, e muito mais. Embora o HTML organize o conteúdo, o CSS define como ele é exibido visualmente.

- **JavaScript**: É responsável por adicionar funcionalidades interativas ao conteúdo HTML. Com o JavaScript, uma página web pode responder a eventos do usuário, como cliques e rolagens, e modificar o conteúdo de maneira dinâmica.


## Resumo: A Importância do HTML na Web
Em resumo, o HTML é a espinha dorsal de qualquer página web. Ele é a fundação onde CSS e JavaScript constroem o visual e a interatividade, respectivamente. Sua importância está em:

1. **Estrutura do Conteúdo**: Cada elemento HTML define a posição e organização do conteúdo.
2. **Semântica**: HTML utiliza tags semânticas para dar significado ao conteúdo, tornando-o acessível e compreensível.
3. **Base da Web**: HTML, CSS e JavaScript formam a base de todo o desenvolvimento frontend.

</br>

<details>
<summary> <strong> Detalhes sobre tags </strong> </summary>

## 1. Tags de Abertura e Fechamento
No HTML, a maioria das tags tem uma **tag de abertura** e uma **tag de fechamento**:

- **Tag de abertura**: `<tag>`
- **Tag de fechamento**: `</tag>`

Por exemplo, uma tag de parágrafo `<p>` aberta é fechada com `</p>`.

````html
<p>Este é um parágrafo.</p>
````
## 2. Tags Auto-Fechadas (Self-Closing Tags)
Algumas tags em HTML não possuem conteúdo entre elas e não precisam de uma tag de fechamento. Elas são chamadas de **tags auto-fechadas** (ou self-closing). Em HTML5, é opcional adicionar uma barra no final dessas tags, mas em XHTML e XML é obrigatório.

Exemplos de tags auto-fechadas incluem:

- `<img>`: Usada para imagens.
- `<br>`: Insere uma quebra de linha.
- `<hr>`: Insere uma linha horizontal.
- `<input>`: Define campos de entrada em formulários.
- `<meta>`: Define metadados sobre a página.
- `<link>`: Conecta folhas de estilo CSS ou outros recursos.

Em HTML5, você pode escrever estas tags auto-fechadas **sem** a barra (`/>`), mas ela pode ser usada se você preferir:

````html
<img src="imagem.jpg" alt="Descrição da imagem">
<br>
<hr>
````
Ou, com a barra final opcional (em estilo XHTML):

````html
<img src="imagem.jpg" alt="Descrição da imagem" />
<br />
<hr />
````
## 3. Tags Omissíveis (Omission Tags)
Algumas tags no HTML podem ser implicitamente fechadas pelo navegador, e você não precisa incluí-las explicitamente. Essas tags incluem:

- `<html>` e `</html>`: Marca o início e o fim do documento HTML. É recomendável incluir, mas muitos navegadores inferem a presença dessas tags.
- `<head>` e `</head>`: Define a seção de cabeçalho da página. Também é preferível incluir, mas alguns navegadores lidam bem sem elas.
- `<body>` e `</body>`: Define o corpo principal do documento.
Por exemplo, em documentos HTML, mesmo sem <html>, <head>, ou <body>, alguns navegadores ainda exibirão o conteúdo. No entanto, seguir a estrutura completa é boa prática e ajuda na organização do código.

## 4. Tags Com Conteúdo Implícito
Existem tags que o navegador pode interpretar como encerradas automaticamente quando uma nova tag é iniciada. O navegador interpreta e fecha essas tags por você. Exemplos comuns incluem:

- **Listas**: Em listas não ordenadas (`<ul>`) ou ordenadas (`<ol>`), cada `<li>` pode ser fechado automaticamente.

````html
<ul>
    <li>Item 1
    <li>Item 2
    <li>Item 3
</ul>
````
Os navegadores interpretam cada `<li>` como encerrado automaticamente antes do próximo `<li>`, mas é recomendado fechar com `</li>` para garantir clareza.

- **Parágrafos**: Em `<p>`, se você iniciar um novo `<p>` sem fechar o anterior, o navegador automaticamente encerra o anterior.

````html
<p>Este é o primeiro parágrafo.
<p>Este é o segundo parágrafo.
````
O navegador trata o primeiro `<p>` como encerrado antes do segundo, mas, novamente, é boa prática fechar cada tag de forma explícita.

## 5. Tags Sem Conteúdo: Tags Inline e Tags de Bloco
Tags no HTML podem ser inline ou de bloco.

- **Tags de Bloco**: Ocupam a largura total do contêiner pai e sempre começam em uma nova linha (por exemplo, `<div>`, `<p>`, `<h1>`). Elas geralmente são usadas para estruturação.

- **Tags Inline**: Não quebram a linha e só ocupam o espaço necessário para seu conteúdo. São usadas para aplicar estilos dentro de linhas de texto (por exemplo, `<span>`, `<a>`, `<strong>`, `<em>`).

Essas características de formatação afetam o layout, mas é importante saber que não têm relação com a necessidade de fechamento das tags.

## 6. Semântica HTML e Tags Obrigatórias
Por fim, a semântica e organização das tags também são importantes. HTML5 trouxe uma série de tags semânticas (como `<header>`, `<footer>`, `<article>`, `<section>`, etc.) para tornar a estrutura mais lógica e fácil de entender, tanto para desenvolvedores quanto para motores de busca e tecnologias assistivas. Essas tags organizam o conteúdo de forma mais significativa e ajudam na acessibilidade.
</details>

</br>

<details>
<summary> <strong> Detalhes sobre o Charset </strong> </summary>

## O Papel do Charset no HTML
Quando você digita, o teclado envia para o computador um conjunto de sinais elétricos, que são interpretados como códigos binários (bytes). Esses bytes precisam ser interpretados para serem exibidos como texto, imagens, som, etc., e para isso, são usadas **tabelas de codificação de caracteres**.

O `charset` (ou conjunto de caracteres) em HTML e em outros contextos serve para informar ao navegador (ou ao programa que está exibindo o conteúdo) **qual é a codificação usada para interpretar esses bytes** e transformá-los nos caracteres visíveis que formam o texto. Esse parâmetro é essencial para que o navegador possa exibir caracteres acentuados e símbolos específicos de forma correta, especialmente em idiomas que usam acentos, cedilhas, e outros caracteres especiais.

## Como o Charset Funciona
O charset mais comumente usado na web hoje em dia é o **UTF-8**. Ele é uma codificação que inclui todos os caracteres da maioria dos sistemas de escrita do mundo e é amplamente compatível, o que resolve a maioria dos problemas de compatibilidade de caracteres. Quando especificamos `charset="UTF-8"` no HTML, por exemplo:

````html
<meta charset="UTF-8">
````
Estamos dizendo ao navegador que todos os bytes no arquivo HTML devem ser interpretados como caracteres no padrão UTF-8. Isso significa que:

1. **Acentos** e caracteres especiais, como é, ç, ã, etc., serão interpretados corretamente.
2. **Símbolos** e caracteres de diferentes línguas, como ñ em espanhol ou 日 em japonês, poderão ser exibidos.

</details>
