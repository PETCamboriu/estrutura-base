# Sistema de Gestão de Eventos Unificado

## Descrição:

Tente colocar a descrição dos futuros projetos da maneira mais clara possível utilizando do principal motivo de sua criação(justificativa no caso), e logo em seguida sua(s) principal(is) funcionalidade(s), de maneira sucinta abortar seu funcionamento sem entrar em termos tecnicos ou que demandem algum conhecimento prévio/específco.

## Descricação da arquitetura

### Motivo de criação:
Bom quem esta escrevendo esse README é um ingresso do ano de 2020, me chamo Gabriel Paz e, quando peguei os projetos do PET percebi uma coisa de cara, além de ser todos em PHP(uma linguagem que não domino), percebi que seu entendimento era complexo além de rigoroso. Os atingos desenvolvedores do PET não se utilizavam de nenhum _pattern_(modelo) para programar esses sistemas, o que é bem perceptivel quando você observa sistemas escritos por pessoas diferentes. 

E foi por isso que eu criei esse repositório, a ideal é utiliza-lo de molde para futuras aplicações/projetos do PET, por que a questão aqui não é entregar o projeto(sim isso é importante, mas não é tudo!), mas sim facilitar a manutenção/compreendimento dos mesmo para os futuros bolsistas, aqui devemos utilizar da regra dos escoteiros:
> Ao sair do lugar onde se chegou o mesmo deve estar mais limpo e organizado do que estava antes de sua chegada.
O que eu quero dizer com isso, é que nos devemos para com esse pensamento de um tanto quando egoísta de querer fazer apenas o serviço que nos pedem sem entregar ele com a melhor qualdade possível, não só para o cliente como tambem para nossos futuros egressos que irão ver não só as minhas gambiras, mas as suas também! Por isso ao criar essa eu utilizei de alguns conceitos:

### Conceitos/ideias usadas

O principal deles é a metodologia **S.O.L.I.D.** que é a base do projeto, sem entrar em detalhes ela diz como manter um código limpo, tambem se o utilizando das práticas do **CleanCode**, organizado, e o principal deles legível para tratamento de erros ou adição de novas funções.

## Tenologias:

__Typescript__: Foi optado pelo typescript pelo ganho significativo de performace na fase de desevolvimento como também as vantagens aparentes no tratamento precoce de erros em em nível de escrita de software,já que o typescript veêm como um superset do javascript acrescentando tipagem estáticas ao ambiente javascript que até o momento possuia um tipagem dinâmica.

__Knex__: Ningume merece ficar escrevendo comando de consulta ao banco em SQL no meio do código, além de não fazer sentido haver SQL no meio do nosso código javascript, chega um ponto onde ele começa a poluir nossa visão. Contudo ele nunca será descartado pois por exemplo quando mais nossa aplicação cresce ela começa a pedir por informação mas especificas coisas que os **ORMs** não lidam tão bem. 
Abaixo segue um exemplo de código com SQL metido no meio, e um com um ORM ajudando:

```js
// Sem a utilização de uma ORM.
const getUser = connection().query('SELECT * FROM users WHERE idade = 18 AND working = false')

// Com uma ORM como o knexJS.
const getUser = knex('users').where({
    idade: 18, 
    working: false
})
```
Concluindo, além de não misturar SQL direto junto com o javascript, ganhamos uma melhor visibilidade sobre o que está sendo tratado na função/comando **getUser**, pois o mesmo é escrito em javascript e transpilado para SQL, permitindo-nos mexer com o banco de uma maneira mais rapida e legível(no ponto de vista de quem programa).

__Migrations__: Estas são uma funcionalidade que alguns dos ORMs atuais no disponibilizam, elas basicamente são a capacidade de manter um historico de alterações/ajustes feitos no banco de dados. Este versionamento de banco(o que não deixa de ser) nos permitir retornar para uma versão especifica do banco onde a mesmo estava funcionando sem problemas, nos ajudando assim a melhor tratar bugs em produção/desenvolvimento.

__Express__: Express é como diz em seu site: 
>  Uma framework para aplicativo da web do Node.js mínimo e flexível que fornece um conjunto robusto de recursos para aplicativos web > e móvel.

Ela é nosso entrada para o mundo das API's, e, como usa-las/desenvolve-las. Com Express nos podemos criar as rotas das nossas aplicações assim como o que será tratado em cada uma delas, esta é a ferramente ideal para quem esta entrado nessa vida com o nodeJS, pois, sua utilização/entendimento é simples e prática, facilitando sua compreensão assim como suas futuras operações e coceitos.