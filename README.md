<h1 align="center">SearchMyName Mundo Livre</h1>
</br>

> ## Solicitações de Projeto
- <i>"Criar aplicação React onde o usuário ao digitar um nome pessoal qualquer em um input de texto, consiga o retorno formatado no frontend da maior probabilidade da origem do nome com o nome do país de origem."</i>

<br/>

> ## Sobre o Projeto
- Projeto de Busca de probabilidade da origem do nome, desenvolvido em React, com o consumo das API <a href= "https://nationalize.io"> Nationalize.io </a>, <a href= "https://www.countryflagsapi.com"> CountryFlagsAPI </a> e utilização dos dados do  <a href= "https://gist.github.com/almost/7748738#file-countries-json"> countries.json </a>. Para a estilização do projeto, optei por utilizar o Bootstrap associado ao CSS com o intuito de deixar a página responsiva.
Usei também Icons da biblioteca "react-icons/bs";

<br/>

> ## Lógicas e Conceitos 
1. No component App.js criei duas funções acionadas pelo click, a primeira openSearch() começa com uma validação para saber se há conteúdo no campo,
e em seguida, como estou trabalhando com uma API, utilizo da programção assíncrona e capturo o nome com a variável "input". Dessa forma, para acessar
as variáveis que irei trabalhar, a "country_id" e a "probability" atribuo cada uma "const nameCountry = response.data.country[0].country_id;"
"const probability = response.data.country[0].probability;" dessa maneira, o que me retorna os primeiros e e maiores incidências dos nomes do obejto;
2. Para acessar o arquivo .json importei o método "useEffect" para poder usar o fetch, e com isso tive acesso ao arquivo, no qual percorrir com um for of,
para identificar qual nome corresponde ao código em questão;
3. A cada ação, envio um setInput("") com o intuito de sempre manter o campus livre;
4. Na segunda função oenCountries() começo atribuindo à variável "valida" o objeto "data" que corresponde ao conteúdo vindo da api, para poder usar a lógica
{Object.keys(valida).length > 0} e fazer o card com os principais países e porcentagens, pois quando for diferente de 0, ele estará disponível para ser mostrado,
e essa ação é ativada com click no botão "onClick={openCountries}". E a cada nova pesquisa essa variável é zerada, para ser preenchia apenas se o usuário tiver interesse.
Assim, sigo com a mesma lógica com o for of, para poder trazer os nomes dos países atrvés do code do arquivo .json;

<br/>

> ## Funcionalidades 
- Encontrar país com maior probabilidade;


<br/>

> ## Funcionalidades Adicionais
- Retorno dos três países com maior probabildiade;
- Consumo da api <a href= "https://www.countryflagsapi.com"> CountryFlagsAPI </a> para rotorno das bandeiras de cada país;
- Layout Responsivo;
- Cálculo da porcentagem dos respectivos países;

<br/>

> ## Tecnologias
<p align="left">
<img alt="react" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img alt="git" src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
<img alt="bootstrap" src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white" />
 </p>

<br/>

> ## Como iniciar esse projeto

    # Clone this repo
    ❯ git clone https://github.com/Guimonteirol/mundo_livre.git

    # Enter on its directory
    ❯ cd searchName

    # Launch the Application    
    ❯ npm start