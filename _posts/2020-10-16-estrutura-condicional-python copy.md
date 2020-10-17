---
layout: post
title: "Estruturas condicionais com Python"
subtitle: Um pouco da teoria de como funcionam as estruturas condicionais, utilizando Python
thumbnail-img: /assets/posts/conditional-structure/estrutura-condicional-thum.png
share-img: /assets/posts/conditional-structure/estrutura-condicional-thum.png
tags: [tutorial, python, overview]
---

![pythonlini1](/assets/posts/conditional-structure/estruturas-condicionais.png){: .mx-auto.d-block :}

![python algoritmo](/assets/posts/conditional-structure/python-algoritmo2.png){: .post-http-small-image :}
Uma Estrutura de Condição, como o próprio nome já diz, verifica a condição dos argumentos passados e, executa um comando caso a condição seja verdadeira. 


Frequentemente, os programas necessitam tomar decisões sobre qual comando executar selecionando duas ou mais ações possíveis de acordo com o resultado recebido.

Sem as estruturas condicionais, os algoritmos/programas sempre executam todas as linhas que escrevemos.

Com as estruturas condicionais, podemos fazer com que algumas linhas do nosso algoritmo não sejam executadas.
![alini-estrutura1](/assets/posts/conditional-structure/estrutura1.png){: .mx-auto.d-block :} 

### Exemplo de um if simples:
![alini-estrutura4](/assets/posts/conditional-structure/estrutura4.png){: .mx-auto.d-block :}

### Álgebra booleana em Python
Para facilitar a estruturação das condições, podemos utilizar os operadores booleanos.
Na tabela a seguir você consegue identificar como eles funcionam:

| Operador  | Python | Exemplo  | Descrição  |
|---|:---|:---|:---|
| E| and|P and Q |Se P e Q forem verdadeiros retorna True, se não retorna False 
|OU| or|P or Q|Se P ou Q forem verdadeiros retorna True, se não retorna False
|Não  | not | not Q |Se Q é verdadeiro retorna False, se não retorna True

<br>

### Exemplo de um if simples em situações compostas:
![exercicios-imc1](/assets/posts/conditional-structure/imc1.png){: .mx-auto.d-block :}


### if composto:

Uma condicional composta é quando juntamos várias condições para chegar á um resultado.
![alini-estrutura5](/assets/posts/conditional-structure/estrutura5.png){: .mx-auto.d-block :}

### Exemplo de um if composto (que tem o else):
~~~
# Imprimir o maior de dois números
n1 = float(input('Informe o primeiro número:'))
n2 = float(input('Informe o segundo número:'))
if (n1 > n2):
    print(n1)
else:
    print(n2)
~~~
<br>

### Encadeamento de comandos condicionais
![exercicios-imc2](/assets/posts/conditional-structure/imc2.png){: .mx-auto.d-block :}

### Encadeamento de comandos condicionais, utilizando "elif"
![exercicios-imc3](/assets/posts/conditional-structure/imc3.png){: .mx-auto.d-block :}

<br>

### Indentação e blocos de código

- No Python, tudo que vem depois de ':' é um bloco de código;
- É como se existisse uma hierarquia dentro do código;
- Se os blocos não forem indentados, irá ocorrer erro no console.
![identação](/assets/posts/conditional-structure/python-identacao.png){: .mx-auto.d-block :}


Em breve iremos construir um projeto simples para iniciar nossa aventura com o Python!
<br>
E agora, vamos codar? ❤️

Grande Abraço, A.R. 🙂
