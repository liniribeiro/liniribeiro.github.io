---
layout: page
title: PiDecor
subtitle: Meu projeto de conclusão de curso da Especialização em arquitetura de Software pela PUC de Minas
gh-repo: liniribeiro/puc-mg-tcc-poc
gh-badge: [star, fork, follow]
---
![image-title-here](/assets/posts/pidecor/pidecor.png){: .mx-auto.d-block :}


# A História

Há alguns anos comecei uma pós graduação em **Arquitetura de Software Distribuído**, pela Puc de Minas.
![fotodaalini](/assets/posts/pidecor/tcc1.png){: .post-medium-image :}
Muitas pessoas me falavam que uma pós graduação não agregaria tanto valor por eu ser DEV.

Como eu já não tenho o background técnico que a maioria dos meus colegas possuem (Por ter feito a graduação de Comercio Exterior) eu insisti em me matricular na Pós.

Como as aulas eram á distância, no decorrer do curso, eu não fui tão comprometida com as elas e depois de alguns meses não estava tão empolgada. Até que chegou a época de fazer o TCC. Não tinha como evitar, até quem não tinha realizado todas as provas e assistido todas as aulas precisava fazer o trabalho.

A proposta era escolher entre dois contextos com destintos requisitos funcionais e não funcionais, a partir de nossa escolha, desenvolver uma proposta arquitetural para eles, juntamente com uma prova de conceito (POC). <br>

![fotodaalini](/assets/posts/pidecor/window.png){: .post-medium-image-left :}
Pois bem, eu fiquei muito ansiosa e passei noites em claro tentando decidir qual dos dois temas seria ideal, qual deles eu encontraria mais detalhes para entender do negócio, qual problema eu teria vontade e alegria em solucionar. Foi difícil mas consegui decidir pelo que possuía um nome maior: Sistema de controle de vendas com a modalidade de entrega dropshipping.

Esta modalidade de entrega de mercadoria é muito utilizada em lojas que não trabalham com estoque, depois que elas recebem o pedido, encomendam a mercadoria com o fornecedor, que por sua vez envia o produto diretamente ao cliente.

O problema que eu escolhi solucionar foi a necessidade de uma solução que engloba todas as informações destas rotinas de venda, logística e engajamento com o cliente, onde concentra todas as informações necessárias para a tomada de decisão, o que dificulta a eficácia na prestação dos serviços.

![fotodaalini](/assets/posts/pidecor/dog.png){: .post-medium-image :}

O sistema será desenvolvido para concentrar em uma única aplicação todas as informações que o usuário precisa ter, sendo ele o cliente da loja, o vendedor externo ou até mesmo o administrador. O sistema tem como objetivo simplificar e impactar positivamente na jornada do usuário ao utilizar o sistema.<br>

O prazo para entrega era 3 meses corridos, onde deveria ser criada a proposta e desenvolver a POC. Em todos estes anos de desenvolvimento, pouquíssimas eram as vezes que eu precisei atuar com front, quase zero, então o desafio maior de todos propostos, era conseguir construir o frontend do meu projeto.

Foram dias e noites na tentativa e erro para aprender a utilizar bootstrap, achar biblioteca que gera PDF, assistindo aulas online de Angular5, e aprendendo a criar charts responsivos, criando autenticação, assistindo aulas online, alterando rotas e testando a implantação do projeto.

**Foram dias e noites incríveis…!**
<br>

# A Execução


**Pidecor**, o e-commerce de decoração com a modalidade de entrega Dropshiping.

![image-title-here](/assets/posts/pidecor/pidecor1.jpg){: .mx-auto.d-block :}
<br>
Em 2015, comprei uma máquina de costura e comecei a fazer algumas almofadas pra vender, foi onde surgiu a **Pidecor**, minha loja de almofadas. 
Era tudo muito lindo e dava um trabalho bem grande.<br>
**Tinha uma loja virtual linda que nunca vendeu se quer 1 almofada!**

![image-title-here](/assets/posts/pidecor/pidecor2.png){: .mx-auto.d-block :}

Foi dali que surgiu a ideia de “personificar” a **Pidecor** como a minha plataforma de e-commerce para iniciar o TCC.<br>

Depois de ter este objetivo identificado, realizei algumas pesquisar e percebi que seria perda de tempo desenvolver um e-commerce, temos hoje muitas plataformas que já disponibilizam toda uma estrutura.

Então pensei por um lado diferente, identifiquei três tipos de usuários para este e-commerce, os clientes da loja, os vendedores externos e o administrador do sistema, que cadastraria fornecedores, analisaria o mondante de vendas e daria suporte para os clientes.

Pensando em toda a jornada do usuário, foi proposto 8 requisitos funcionais, de acordo com o papel do usuário.

![image-title-here](/assets/posts/pidecor/requisitos-pidecor.gif){: .mx-auto.d-block :}

Um dos requisitos  solicitados para o trabalho era que o sistema seja integrado com outros dois sistemas:
- De Fornecedores: que fornece os produtos da loja e promovem a entrega.
- De monitoramento: que gera as informações gerenciais sobre os resultados das vendas e eventos de entrega.


Para obter as informações dos fornecedores e criar esta integração, construí uma mock que simula a API de fornecedores e disponibiliza os seus serviços utilizando o protocolo **SOAP**.<br>
![fotodaalini](/assets/posts/pidecor/plants.png){: .post-medium-image-left :}
Já na integração com o sistema de monitoramento, foi utilizado o Postman para simular os serviços que recebem as informações gerenciais e criei um agendador que envia para o sistema de monitoramento estas informações todos os dias no mesmo horário.

- O projeto está todo [dockerizado](https://hub.docker.com/repository/docker/aliniribeiroo/pidecor-admin), e está utilizando o docker-compose para sincronizar e facilitar o controle dos serviços;
- Disponibilizei o código e o roteiro de implantação no meu [github](https://github.com/liniribeiro/pidecor);
- Para visualizar o vídeo que eu criei para a pré apresentação do projeto está no [Youtube](https://www.youtube.com/watch?v=Hv1tI7ID35c).

No dia da apresentação eu estava super nervosa, coração na mão e com medo de que ao mostrar minha aplicação, algo errado acontecesse. Eram 10 horas da manhã e meu skype começou  a chamar, era a apresentação online com os professores, e o tempo era bem limitado.

Nervosa comecei a explicação e a apresentar a aplicação, no final veio o feedback do professor:

Ficamos todos muito felizes e impressionados com o seu trabalho. Você se preocupou com a jornada do usuário e construiu bem mais do que o esperado. Parabéns!

Aquele dia foi realmente o melhor dia do ano, sai de casa super feliz e sorrindo no caminho do trabalho, na semana seguinte a minha surpresa. **9.3**!

**Em resumo, nestes três meses de arquitetura e desenvolvimento eu aprendi muitas coisas, me diverti, me senti uma super-heroína e depois uma burrinha e depois uma super-heroína de novo e juntando tudo isso, tirei uma nota super acima do que o esperado e hoje eu sei que sou capaz de qualquer coisa!** 

O vídeo de apresentação do trabalho se encontra no [Youtube](https://www.youtube.com/watch?v=Hv1tI7ID35c) e o código com todo o projeto em meu [github](https://github.com/liniribeiro/puc-mg-tcc-poc)! 