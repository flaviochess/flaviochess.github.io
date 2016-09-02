---
layout: post
title:  "Jekyll: Ferramenta para Criação de Blogs"
date:   2016-09-02 00:00:00 -0300
categories: github
---

No post anterior comentei sobre este blog que é hospedado no GitHub Pages.

Agora se você, assim como eu, não quer ter o trabalho de criar toda uma estrutura de páginas para criar um blog, não se preocupe pois existem ferramentas que facilitam este trabalho, uma delas é o Jekyll.

### Sobre o Jekyll

Acredito que o Jekyll não é do GitHub, mas vi que ele é bem popular e existem outras ferramentas que o tem como base, além de ter visto uma citação dele na própria documentação do GitHub quando me deparei com um erro em outra situação. Estes fatos me fizeram escolher ele para montar este blog.

### Facilidade

O Jekyll funciona como estes geradores de projetos existentes em várias linguagens que te dá uma estrutura de um projeto pronto, mas como é um blog ele não te dá uma simples estrutura, mas sim tudo de bandeja cabendo a você apenas criar os posts.

Os posts são escritos em <a href="https://guides.github.com/features/mastering-markdown/" target="_blank">markdown</a> o que facilita a formatação dos textos.

Além de gerar todo o blog já pronto para você apenas *commitar* no seu repositório do GitHub também permite subir o blog localmente com apenas um comando para testar antes de subir o projeto para “produção”.

### Sobre a Instalação

Para usar o Jekyll você precisa basicamente de um sistema operacional **Unix-like** e do Ruby. Se por algum motivo você é um desenvolvedor que utiliza Windows ainda, é possível de uma forma não oficial porém citada pelo próprio site do Jekyll de usar-lo. 

Já se não utiliza o Windows basicamente precisa se preocupar apenas com a parte do Ruby (que será utilizado pelo Jekyll para baixar outras dependências), os demais requisitos costumam existir por padrão nestes sistemas.

Os requisitos completos e também como usar o Jekyll no Windows podem ser vistos <a href="https://jekyllrb.com/docs/installation/" target="_blank">aqui</a>. 

### Customização

O blog gerado nada mais é que um amontoado de HTML e CSS. E estes se preferir podem ser alterados para mudar o layout do seu blog (podem perceber que eu não fiz isso rs). O conceito é que ele apenas gera o código inicial pra você e daí pra frente o que você vai fazer com este código é problema seu.

### Alternativas

A verdade é que o Jekyll foca no essencial, sem muitas firulas. Porém existem muitas alternativas a ele, inclusive alternativas que por baixo usam o Jekyll, vejo como uma extensão do mesmo.

O único que cheguei a experimentar foi o <a href="https://tinypress.co/" target="_blank">TinyPress</a>, que tem como o mais atrativo você não precisar da linha de comando nem sequer instalar nada. Você cria uma conta no site deles, dá permissão para acessar seu repositório do GitHub e no próprio site do TinyPress você escreve seus posts e envia por lá mesmo, totalmente web. Só não gostei dele pedir permissões para acessar meus repositórios privados também, mas enfim.

Com uma busca rápida no Google encontrei já no primeiro link outras <a href="https://www.sitepoint.com/6-static-blog-generators-arent-jekyll/" target="_blank">seis alternativas</a>. Destes seis já ouvi falar também do Octopress.

### Mais Informações

Até por sua simplicidade a documentação do Jenkyll é bem completa, porém em inglês. Nada que seja um grande empecilho para quem não domina a língua pois são textos curtos e com muitos exemplos.

* Site oficial do Jekyll: <a href="https://jekyllrb.com/" target="_blank">https://jekyllrb.com/</a>;
* Documentação: <a href="https://jekyllrb.com/docs/home/" target="_blank">https://jekyllrb.com/docs/home/</a>;
* Instalação: <a href="https://jekyllrb.com/docs/installation/" target="_blank">https://jekyllrb.com/docs/installation/</a>.