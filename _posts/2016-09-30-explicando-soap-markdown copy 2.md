---
layout: post
title: "Explicando: SOAP"
subtitle: Overview sobre o protocolo de comunicação baseado em XML
gh-repo: liniribeiro/soap_mock
gh-badge: [star, fork, follow]
thumbnail-img: /assets/posts/soap/soap-thu.png
share-img: /assets/posts/soap/soap-thu.png
tags: [overview, protocol, soap]
---
![cocos2dlini1](/assets/posts/soap/soap-alini.png){: .mx-auto.d-block :}

Olá pessoa! Hoje vou escrever um pouco sobre o Simple Object Access Protocol (SOAP) significa Protocolo Simples de Acesso a Objetos, é um protocolo de comunicação baseado em XML que permite a comunicação de mensagens entre aplicações via HTTP  utilizado em WebServices.


A comunicação entre o web service e o Client acontece apenas por mensagens XML, uma arquitetura simples de web service que possui apenas dois componentes: o Client e o Service Provider

Em nossa comunicação, o cliente tenta se comunicar com o Service Provider, mas para isso ele precisa de algumas informações como:
- Local do WebService server
- Funções disponíveis, assinatura e o que é retornado das funções
- Protocolo de comunicação
- Formato de entrada e saída

O Service Provider cria um arquivo XML padrão tem todas essas informações, então, se esse arquivo é entregue para o Client ele poderá acessar o web service. Esse arquivo XML é chamado de WSDL.


## O QUE É WSDL?
WSDL é a sigla para Web Service Description Language, é um arquivo XML que descreve em detalhes técnicos como implementar o web service, mas especificamente a URI, porta, nome dos métodos, argumentos e tipo dos dados.

Desde que WSDL é um XML, os dois são legíveis por humanos e consumíveis por máquinas o que ajuda na manipulação destas informações de uma forma dinâmica.
Usando o arquivo WSDL podemos entender coisas como:
- Porta;
- URL do web service;
- Formato de entrada;
- Formato de saída;
- Protocolo de segurança que deve ser seguido;
- Qual protocolo o web service usa.


## MANEIRAS DE ACESSAR UM WEB SERVICE

Existem duas maneiras de acessar um web service, a primeira é quando o Provider conhece o Client ele entrega o WSDL para o Client que terá todas as informações para acessar o web service.
Já a segunda é quando o Provider registra a WSDL no UDDI, que é onde os servoços são registrados, então o Client procura pelo registro:

- Service Provider registra no UDDI;
- Client procura pelo serviço no UDDI;
- UDDI retorna todos os provedores que estão oferecendo o serviço procurado;
- Client escolhe o Service Provider;
- UDDI retorna a WSDL escolhida;
- Usando o WSDL do Service Provider o Client acessa o web service.



# WEB SERVICE SOAP EM JAVA COM ECLIPSE

Segue como podemos criar um web service SOAP em java, utilizando o eclipse:
- Criar um novo “Dinamic Web Project” no eclipse, coloque o nome de seu projeto;
![cocos2dlini1](/assets/posts/soap/soap1.png){: .mx-auto.d-block :}

- Criar um novo pacote com o nome: exemplo.javapost.webservices;
![cocos2dlini1](/assets/posts/soap/soap2.png){: .mx-auto.d-block :}

- Criar uma classe chamada “HelloWorld.java”;
![cocos2dlini1](/assets/posts/soap/soap3.png){: .mx-auto.d-block :}

- Clicar com botão direito no projeto > Novo > Web Service;
![cocos2dlini1](/assets/posts/soap/soap4.png){: .mx-auto.d-block :}

- Em Service Implementation, colocar o nome do pacote que você criou, junto com o nome da classe: exemplo.javapost.webservices.HelloWorld;
- Nos níveis de Test service e Test Client, colocar no nível máximo e clicar em Finish. Um novo projeto chamado ExemploSOAPClient foi criado na sua workspace;
- Depois de iniciar o server, você poderá testar seu projeto.
![cocos2dlini1](/assets/posts/soap/soap5.png){: .mx-auto.d-block :}
![cocos2dlini1](/assets/posts/soap/soap6.png){: .mx-auto.d-block :}

Prontinho, achei super fácil criar e testar o web service, o que me deixou feliz.
Grande Abraço, A.R. 🙂
