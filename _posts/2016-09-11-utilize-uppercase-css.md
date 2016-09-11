---
layout: post
title:  "Utilize Uppercase no CSS!"
date:   2016-09-11 00:00:00 -0300
categories: CSS
---

Hoje eu vim trazer uma dica que aprendi e achei muito importante: **para deixar um texto maiúsculo, não escreva em caixa alta, utilize CSS!**

Atualmente, todo desenvolvedor sabe a importância de usar o atributo alt na tag img do HTML. Se você não sabe deveria saber:

>Utilizamos o atributo alt para descrever a imagem em questão com o principal objetivo de tornar nossas páginas mais acessíveis (ou pelo menos este deveria ser o principal motivo) pois deficientes visuais também navegam pela internet porém usando programas ou plugins que leem o conteúdo da página e quando encontra uma imagem ele lê o atributo alt dela para o usuário. 
Além dos deficientes visuais os robôs dos buscadores como o Google também leem este atributo para auxiliar nas buscas.

Acontece que o que costuma ter letras maiúsculas são siglas como HTML, CSS, CPF, entre outras, e ao encontrar um texto em maiúsculo os leitores de conteúdos de deficientes visuais irão ler como lemos, letra a letra: F G T S. Estas siglas devemos escrever no HTML em maiúsculas mesmo.

Porém existem também aqueles casos em que desejamos ter um título todo em maiúsculo por questões de estética, casos que não se tratam de siglas. Nestes casos não escreva todo em letra maiúscula no HTML pois isso ocasionará uma confusão nos leitores de conteúdo que tentarão ler letra a letra. Para ter o efeito de maiúsculo utilize o CSS:

```css
/* colocando todos os H1 em letra maiúscula */

h1 {
	text-transform: uppercase;
}
```

Desta forma o HTML terá sua escrita em minúsculo fazendo com que os programas consigam ler corretamente e as pessoas sem deficiência visual enxergarão como você deseja!
