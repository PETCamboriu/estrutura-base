# Descricação da arquitetura

### Motivo de criação:
Bom quem esta escrevendo esse README é um ingresso do ano de 2020, me chamo Gabriel Paz e, quando peguei os projetos do PET percebi uma coisa de cara, além de ser todos em PHP(uma linguagem que não domino), percebi que seu entendimento era complexo além de rigoroso. Os atingos desenvolvedores do PET não se utilizavam de nenhum _pattern_(modelo) para programar esses sistemas, o que é bem perceptivel quando você observa sistemas escritos por pessoas diferentes. 

E foi por isso que eu criei esse repositório, a ideal é utiliza-lo de molde para futuras aplicações/projetos do PET, por que a questão aqui não é entregar o projeto(sim isso é importante, mas não é tudo!), mas sim facilitar a manutenção/compreendimento dos mesmo para os futuros bolsistas, aqui devemos utilizar da regra dos escoteiros:

> Ao sair do lugar onde se chegou o mesmo deve estar mais limpo e organizado do que estava antes de sua chegada.

O que eu quero dizer com isso, é que nos devemos para com esse pensamento de um tanto quando egoísta de querer fazer apenas o serviço que nos pedem sem entregar ele com a melhor qualdade possível, não só para o cliente como tambem para nossos futuros egressos que irão ver não só as minhas gambiras, mas as suas também! Por isso ao criar essa eu utilizei de alguns conceitos:

### Conceitos/ideias usadas

O principal deles é a metodologia **S.O.L.I.D.** que é a base do projeto, sem entrar em detalhes ela diz como manter um código limpo, tambem se o utilizando das práticas do **CleanCode**, organizado, e o principal deles legível para tratamento de erros ou adição de novas funções.

### Explicação sobre as pastas desta arquitetura

Bom vamos lá pessoal começaremos pelo começo, sim, a pasta **src**, bom dentro desta pasta é onde deve constar todo o nosso código seja ele _backend_ é claro dentro dela podemos ver algumas subpastas como o:
### **database**
Como o próprio nome já diz nela consta todos os nosso arquivos/informações sobre nosso banco de dados, incluindo nela as pasta **migtaions**(para o versionamento do nosso banco de dados), **models/enetities**(onde ficam nossos "modelos/entidades" de tabelas como users, ou companies), e por fim temos o arquivos **connection** que o proprrio nome já fala por si, ele é nosso conexão com o banco.
### **provider**
Nesta pasta nós temos nossos arquivos que são responsáveis por fazer alguma funcionalidade no sistema, como por exemplo envio de email, então temos a pasta **sendEmail** e dentro desta página teremos todos os arquivos envolvido com o envio de emails como por exemplo o sendEmail, e o getUserEmail. Então para cada novo "micro-serviço" ou funcionalidade no sistema criamos uma nova pasta como por exemplo verificar o email do novo usuário registrado.
### **repositories**
Em repositories ficam os arquivos de tratamento de funções no nosso banco de dados como por exemplo inserir um novo usuario, respeitando a criação de pastas para cada tabela do banco banco, por exemplo na pasta User nos tratamos de funções/operações na tabela de usuario como por exemplo inserir ou pegar todos os emails dos usuarios registrados, onde cada arquivo representa uma funcionalidade que é exportada para o arquivo index da pasta, a ideia de fazer tal organização é tentar ao maximo o reaproveitamento de código pelo sistema.
### **routes**
Presente nesta pasta constam nossos arquivos que ditam que rotas pessoas com permissão administrativa podem frequentar, assim como pessoas com permissão pública.

<hr>
Continuando a explicação sobre a organização de pastas agora vamos para as de **__test__**, **build**, **dist**, **node_modules** e por fim **images**, let's go começando pela a pasta node_modules:

### **node_modules**
Esta pasta é simples de se entender, bom todos os modulos ou dependencias que necesistarmos usarmos durante o desenvolvimento dos nossos projetos vão pra essa pasta, em resumo ela é responsável por guardar e gerir todos os modulos que necessitarmos durante a criação dos projetos.
### **images**
Na pasta _images_ é onde podermos guardas screenshots ou gifes sobre funcionamento da nossa aplicação a fim de mostra-lo(a) no README do projeto.
### **__test__**
Bom Nesta pasta ficam todos os testes de aprovação do sistema, são estes teste que permitem a nos garantir um melhor resultado e tratamento de bugs antes do software sair para produção e até mesmo durante.
### **dist**
Na pasta chamada _dist_ é onde nos podemos colocar nosso código typescript compilado em javascript antes mesmo dele ir para produção.
### **build**
E por e não menos importanten a pasta _build_ que é onde fica nosso software completo após passar por todos os seus testes, e compilação, está pasta é aquele que será enviada para ser usada na produção.


# <Nome do programa/>

## Descrição:

Tente colocar a descrição dos futuros projetos da maneira mais clara possível utilizando do principal motivo de sua criação(justificativa no caso), e logo em seguida sua(s) principal(is) funcionalidade(s), de maneira sucinta abortar seu funcionamento sem entrar em termos tecnicos ou que demandem algum conhecimento prévio/específco, algo que pode ajudar futuros desenvolvedores é a utilização de um gife que nos permita ver o funcionamento principal do sistema.

## Tenologias:

Ao entrar nas tecnlogias utilizadas a melhor maneira de mostra-las é, aborte de maneira rápida e direta o motivo da sua utilização não esquecendo de dar um motivo válido, além de mostrar onde é utilizada e o que faz no projeto, sempre pensando que futuramento novas funções, correções ou até mesmo migrações podemo vir, e estar bem informado sobre as tecnologias dos projetos facilitará ou até mesmo evitará mograções futuras.