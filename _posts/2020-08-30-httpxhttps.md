---
layout: post
title: "HTTP x HTTPS"
subtitle: Segurança na comunicação com o Servidor
thumbnail-img: /assets/posts/http/http-https-thumb.png
share-img: /assets/posts/http/http-https-thumb.png
tags: [web, http, overview]
---
![pythonlini1](/assets/posts/http/http-https.png){: .mx-auto.d-block :}

#### HTTP x HTTPS

Como vimos na sessão anterior, o HTTP é um protocolo de comunicação em uma arquitetura Cliente-Servidor. Esta comunicação é realizada com texto puro, e qualquer tipo de dado pode ser enviado para um servidor, até mesmo dados confidenciais, como uma senha. 
Essa informação está aberta no Cliente e pode ser visualizada pela ferramenta do desenvolvedor, que fica disponível nos nossos navegadores. Podemos analisar todas as informações enviadas pelo servidor, na aba Network. 

Quando fazemos o Login em um site, o Cliente envia estes dados para o Servidor realizar uma validação, porém, até este dado chegar no servidor, ele já passou por vários outros servidores intermediários. Da mesma forma acontece com a resposta, ela passa por vários servidores até chegar de volta em nosso navegador. O problema nesta comunicação é que, utilizando o HTTP este dado fica aberto e qualquer pessoa pode espiar nossas mensagens, o que é muito Inseguro.

![http-methods](/assets/posts/http/post-https.png){: .post-http-small-image :}

Podemos fazer uma analogia com o envio de uma carta de São Paulo para Blumenau:
- A carta será postada no correio mais próximo;
- É enviada para a central de São Paulo;
- É encaminhada para a Central de Florianópolis;
- É direcionada para Blumenau
- Finalmente é entregue em sua casa.

Então nossa carta ficou passeando por vários lugares até de fato chegar no destinatário, e em todos esses lugares alguém estava dando uma espiada no que tinha dentro dela.
Pra resolver este nosso problema, existe o HTTPS, que é a mesma coisa que o HTTP, porém, com uma camada a mais de segurança. 

#### Certificado Digital

Para garantir a segurança dos dados, o HTTPS utiliza uma criptografia baseada em chaves públicas e privadas. Paras que estas chaves sejam geradas, de alguma forma é preciso ter uma garantia de quem tá pedindo por esta geração. É preciso garantir que o site da Alini está mesmo tentando se comunicar com o Servidor da Alini. Esta identificação é realizada a partir de um Certificado digital.
![cert1](/assets/posts/http/certificado.png){: .mx-auto.d-block :}

>Um certificado digital prova uma identidade para um site, onde temos informações sobre o seu domínio e a data de expiração deste certificado.

Então, o Certificado digital é utilizado para identificar a entidade e também para gerar as chaves para a criptografia dos dados.

Apenas conseguimos um certificado digital, a partir de uma **Autoridade Certificadora**, que é um órgão confiável que garante a identidade do site e também a validade do certificado.
![cert2](/assets/posts/http/certificado1.png){: .mx-auto.d-block :}

Então quando utilizamos o HTTPS o envio das mensagens funcionam da seguinte forma:
- O Cliente em posse da chave pública criptografam as informações e as enviam para o servidor
- Servidor as descriptografa com a chave privada.
Apenas a chave privada pode descriptografar as informações criptografadas com a pública.

![http-methods](/assets/posts/http/keys.png){: .mx-auto.d-block :}

Grande Abraço, A.R. 🙂
