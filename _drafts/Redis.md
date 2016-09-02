Redis

O Redis é um banco de dados NoSQL. Isso provavelmente você já saiba! Também deve saber que ele possui uma estrutura de chave-valor, mas o que normalmente acontece é das pessoas não saber todo o pontencial do Redis e o porque utilizariam ele!

Neste post vou falar brevemente sobre o que é o Redis e como andam usando ele por aí para melhorar muitas aplicações.

### Estruturas

No Redis a estrutura básica e mais famosa é a chave-valor, isto é, basicamente você informa uma chave única e o valor que será armazenado para aquela chave. Para buscar este valor você informa a chave que foi utilizada e o Redis te devolve o valor (similar a um Map encontrado em muitas linguagens):

[imagem chave-valor]

Existe também a estrutura de hashes que eu denomino como chave-campo-valor ou um map de maps. Esta é uma estrutura mais complexa exemplificada na imagem abaixo:

[imagem hash]

### Soluções com Redis

Quando ouvi falar do Redis pela primeira vez fui procurar saber mais a respeito e encontrava exatamente o que eu resumi acima. Nada que motivasse a utilizar-lo.

Foi apenas quando eu vi sendo utilizado na prática que entendi o quão interessante ele podia ser para os projetos. Por isso resolvi contar algumas formas de se utilizar o Redis.

#### Cache de sistema

Talvez este seja o uso mais clássico do Redis. Imagine uma busca simples que é feita a todo momento e retornam sempre os mesmos dados ou dados que variam pouco. Estes tipos de dados costumamos jogar na sessão enchendo a memória do servidor ou buscamos toda vez no banco de dados.

A alternativa para isso tem sido o Redis, gravando como chave a identificação do objeto, algo como **idUsuario:45785** e o valor desejado, podendo até ser um objeto inteiro, pois quando falamos de chave-valor no Redis, o valor é um string, então podemos colocar lá o que quisermos (desde que como string), podemos serializar um objeto e colocar lá, podemos gravar um objeto como um JSON, ou simplesmente armazenar apenas um valor desejado e não todos os dados.

Você pode me perguntar: *e por que não utilizar um banco de dados convêncional com uma super tabela que contém um campo pra chave e outro pro valor?* 
Simples, o Redis é extremamente mais rápido (é assustador ver a velocidade) do que qualquer outro banco diferente. Isso porque ele trabalha com os dados em memória, ele persiste os dados em disco é claro, mas mantém a cópia em memória, então é muito mais rápido buscar os dados de uma meméria RAM do que ir em qualquer banco buscar estes dados.

Então pode me vir outra pergunta: *se os dados estão em memória, porque não usar a própria sessão do servidor?* 
A resposta para esta é: Escalabilidade!

Um caso mais simples seria, ao invés de você manter um amontoado de dados na sessão do servidor da sua aplicação concorrendo com o processamento dela, você pode ter um Redis em outro servidor e deixar a memória livre totalmente para o processamento da sua aplicação.

Um caso mais complexo seria ter dois ou mais servidores para a sua aplicação devido a alta demanda e um load balance no meio. Se você gravar os dados na sessão o usuário teria que ficar preso a aquele servidor, o que perderia todo o conceito e provavelmente muito trabalhoso de se configurar isso. 
A outra alternativa seria replicar a sessão entre os servidores, fazendo com que você tenha dados repetidos entre eles. Como solução você pode ter uma sessão compartilhada através do Redis. Neste caso você deixa de salvar as coisas na sessão e grava apenas no Redis e seus servidores consultam um local em comum sem duplicar dados.

Além destes casos a sessão de servidores basicamente se limita a colocar um dado lá, consultar e retirar, já no Redis veremos nos próximos casos que ele vai além disso.

// exemplo de carrinhos de compra de ecommerce
// contador de visitas
// gravar resultados de quantidade e etc
// youtube
//controlar inatividade do usuário