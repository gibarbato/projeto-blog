# projeto-blog
projeto-blog

Criação de uma página web que contenha um input para titulo e outro para escrever um conteúdo. Vamos simular a criação de um post semelhante ao facebook, linkedIn... Onde daremos um título, e escreveremos um texto qualquer e postamos, comunicando com uma API aberta. Simulando um pouco do mundo real.

Obrigatório usar JavaScript.

Introdução

Este desafio é interessante, pois estaremos utilizando a família completa do front-end. A base para se fazer qualquer App que consome API's. Relaxe pequeno gafanhoto, que não será o bixo de 7 cabeças; Mas, te levará ao próximo nível, com certeza!

Os requisitos mínimos para avaliar a sua página dinâmica seriam:

1 Basicamente no html, precisaremos de algum lugar para entrada de dados (input). E, outro para saída (output) 1.1 Para a entrada, teremos form, dois inputs de texto e um botão para requisição post; 1.2 Para saída de renderização, teremos alguma tag de título para receber o título; e outro de parágrafo para receber o conteúdo.

2 No js, precisaremos de seletores. 2.1 Um, para aplicar evento de submit. 2.2 Outros dois, para retirar título e conteúdo que quero enviar em meu post 2.3 Outros dois, para renderizar o retorno do post, também titulo-renderizar e conteudo-renderizar.

📘 Especificações

Especificações dos requisitos mínimos

1.1 Vale ressaltar, que é para fazer o form. Você pode utilizar para o conteúdo um textarea ao invés de input de texto. Utilizar um button ao invés de input de submit, utilizar um button mesmo... Vai de cada freguês, de testes, de erros e acertos!!! Caso, queira seguir algum fórmula:

<form><input type='text'><input type='submit'>
1.2 Para renderizar, é livre também! Porém, alguma fórmula?

<h2></h2>
<p></p>
Para que não criemos dinamicamente, os elementos que precisamos para renderizar o conteúdo que será retornado do fetch/post, você pode ter algum h1,h2,h3... Para receber o título. E, algum p, div, article, textarea, ou o que for, onde você poderá receber o valor retornado do seu post, como no exemplo acima. Porém, deve sempre identificar com o seu id (identificador único);

<h2 id="renderizador-titulo"></h2>
Já no js, algumas especificações para se pensar:

2.1 Os seletores essenciais para qualquer dinâmica ou troca de dados que eu queira fazer entre os documentos html e js.

const renderizadorTitulo = document.querySelector('#renderizador-titulo')
// e por aí vai!!!!
2.2 Deve-se adicionar um evento de "addEventListener" para submeter o conteúdo que está no form. 2.3 Não esquecer de capturar o event, ou e, para poder prevenir o comportamento padrão do formulário (preventDefault). 2.4 Ao criar um post, você deve montar o seu objeto! 2.4.1 A estrutura do objeto que você enviará na sua chamada de API post, deve ser a seguinte:

const data = {
        title: titulo.value,
        body: conteudo.value, 
        userId:1
    }
Não mude o nome de data, nem title, nem body e nem userId. Deixe os elementos como estão. A única coisa que pode varia é titulo.value ou conteudo.value que seriam os valores dos seletores que você criou. Se seu seletor se chamar, tituloPost. Então, ficaria tituloPost.value!

Para o nosso fetch, precisaremos ficar atentos às nossas configurações:

url: https://jsonplaceholder.typicode.com/posts
method: "POST"
body: JSON.stringify(data)
headers: {"Content-type": "application/json; charset=UTF-8"}

Em nosso segundo then é onde ocorre a nossa mágica :)

Onde juntos, renderizamos o nosso post enviado!

// renderização 
tituloRenderizar.innerHTML = data.title
Lembrando, que tituloRenderizar, significaria o seletor de onde eu gostaria que os meu titulo postado fosse renderizado!

*📘 Dicas

1. Utilize sempre as tags que apresentam semântica, aprendidas durante o curso:

<nav><main><section><article><aside><footer>
2. Como as interações entre html e js dependem das classes ou ids. Por favor, reforço o uso de id ou class onde forem necessários.

<p id="renderizador-conteudo"></p>
3. Não se faz obrigatório, porém, é interessante utilizar sempre que possível a acessibilidade.

<input type="image" value="Enviar agora" alt="Enviar o post">
4. No curso, você aprendeu a criar uma classe que empacotava os métodos SELECT, POST, PUT e DELETE. Se quiser utilizar, fique a vontade, também não é obrigatório para este desafio. O mais importante, é que haja interação html e js. E que você consiga fazer um fetch, isto é, uma busca, na url passada acima. Então, a dica é revisar as aulas sobre "fetch"

<input type="image" value="Enviar agora" alt="Enviar o post">
5. Digamos que o CSS, não é o mais importante. Não dei dicas, e não fiz olho grosso. Mas, o mínimo é sempre bom, pelo menos para não ficar tão grosseiro. Um padding, uma margin entre os elementos, alguma fonte diferente. Deixar minimamente trabalhada, ok! E claro, pode cleanar! Isto, fazer a limpa css padrão do curso... Para, você dar a seu padrão css!

* {
    box-sizing: border-box;
}

body {
    font-family: system-ui;
    margin: 0;
}
📘 Entrega

Com seu repositório GitHub em mãos, você deve criar um repositório chamado posting--page e adicionar na branch main/master seus arquivos index.html, style.css e o main.js contendo a solução do projeto. Claro que se você quiser, pode enviar a pasta contendo ambos os arquivos. Configure o repositório como público e insira o link para ele no campo Link da solução. Lembre-se de adicionar o link completo, começando com https://. Ele será parecido com isto:

https://github.com/nomedeusuario/posting--page
👉🏻 Dica 1: Se você quer sempre ir testando, conforme você está produzindo o seu conteúdo, é possível você baixar uma extensão super útil em seu Visual Studio Code chamado Live Server. Uma vez instalado, basta abrir o explorador do VSCode, clique com botão direito sobre o seu arquivo index.html e escolha a opção "Open with Live Server" ou "Abra com seu Live Server". Caso, não tenha um editor como o VSCode em sua máquina, é possível utilizar um editor online. Exemplo, https://codepen.io/ ou a https://jsfiddle.net/. Faça um teste antes e verifique se este editor online faz integração com sua conta github para entrega do seu desafio final.

👉🏻 Dica 2: Você pode procurar por "Como criar um arquivo readme.md" no Google e aprender uma habilidade nova. Assim, você pode criar um arquivo readme.md contendo toda a explicação sobre o seu projeto e como executá-lo. Isso será um diferencial muito interessante para o seu projeto que chamará a atenção de futuros recrutadores. Este, caso, você tenha feito num editor online, pode ser criado no próprio github.



git clone 
git status 
git add .
git status 
git commit -m " mensagem aqui "
git checkout -b nome-da-branch-nova
git push origin  nome-da-branch-nova
