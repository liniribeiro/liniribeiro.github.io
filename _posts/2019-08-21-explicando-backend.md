---
layout: post
title: "Explicando: Backend"
subtitle: Uma explicação simples do que é um Backend!
gh-repo: liniribeiro/wheather
gh-badge: [star, fork, follow]
thumbnail-img: /assets/posts/backend/backend-alini-thu.png
share-img: /assets/posts/backend/backend-alini-thu.png
tags: [programacao, overview]
---
![pythonlini1](/assets/posts/backend/backend-alini.png){: .mx-auto.d-block :}

Trabalhei muitos anos com aplicações Desktop e quando decidi trabalhar com desenvolvimento Web, foram alguns meses até conseguir assimilar tudo o que estava fazendo e me apaixonar mais ainda por desenvolvimento, especialmente o desenvolvimento do backend das aplicações. Mas o que envolve o backend de uma aplicação?


O backend de uma aplicação disponibiliza API’s para que o frontend consumir. É no backend que se encontra toda a regra de negócio e acesso á base de dados.

Mas o que é uma API? Aplication Programing Interface é um conjunto de definições e protocolos usados no desenvolvimento e na integração de software de aplicações. Tem um post muito explicativo sobre API’s da Red Hat que eu indico muito a leitura.

Para explicar melhor o o fluxo de comunicação entre frontend  e backend, vamos utilizar uma aplicação web que apresenta a temperatura de cidades:

Esta aplicação precisa salvar as cidades favoritadas, acessando um **banco de dados** e fazer integração com uma API de terceiros, que nos disponibiliza em tempo real as temperaturas da cidade, a OpenWheatherMap.

![pythonlini1](https://user-images.githubusercontent.com/10133177/48674225-ebb0f300-eb30-11e8-912a-a1c7c09f412f.gif){: .mx-auto.d-block :}

Em nosso exemplo, possuímos personagens principais que irão se conectar para que possamos apresentar todas as informações para o usuário:

- Frontend: interface visual;
- Backend: contém a lógica de negócio e integração com os demais personagens;
- API de terceiros:  Nos informa as cidades e temperaturas;
- **Banco de Dados**: Armazena as informações das cidades favoritadas pelo usuário.
 

A comunicação entre aplicações irá se comportar da seguinte forma:
![pythonlini1](/assets/posts/backend/comun-app-alini.png){: .mx-auto.d-block :}

Para realizar esta tarefa de salvar e apresentar as cidades, vamos precisar construir 4 APIS no backend:

- API que retorna todas as cidades disponíveis;
- API que salva uma cidade como favorita;
- API que retorna a lista de cidades favoritadas;
- API que retorna a temperatura de uma cidade;
- API que deleta uma cidade favorita.
- Vamos aos detalhes desta comunicação:

A primeira API vai ser chamada pelo frontend, e será responsável por chamar a API do OpenWheatherMap   que irá retornar todas as cidades disponíveis para serem apresentadas para o usuário, que poderá escolher a cidade que ele deseja favoritar.

Na ação de favoritar do usuário, o frontend chamará nossa segunda API, que salva uma cidade favorita no **banco de dados**.

Após ser feita a ação de favoritar a cidade, nosso frontend apresenta uma lista de todas as cidades favoritadas para o usuário, e ele faz isso utilizando nossa terceira API, que busca na base de dados a lista de todas as cidades favoritadas.

Com cidades cadastradas, agora é a hora de nosso usuário visualizar a previsão do tempo de uma das cidades escolhidas. Quando o usuário entra no detalhamento de uma Cidade, utilizamos a nossa quarta API, que é responsável por retornar a temperatura atual da cidade.
Como esta informação deve ser em tempo real, o backend irá se comunicar com a API do OpenWheatherMap solicitando a previsão do tempo para a cidade específica

E por fim, disponibilizamos a opção de o usuário remover uma cidade favorita, pela nossa última API que acessa o **banco de dados** para remover a cidade.

Desta forma conseguimos seguir a trilha de comunicação entre as aplicações.Este exemplo está postado em meu Github, e a documentação das API’s está na Wiki do projeto.

Grande Abraço, A.R. 🙂