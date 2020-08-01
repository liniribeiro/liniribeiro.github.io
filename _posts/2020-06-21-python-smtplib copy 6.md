---
layout: post
title: Python - Enviando emails com SMTPLIB
subtitle: Tutorial de um código simples em menos de 10 minutos!
gh-repo: liniribeiro/email-with-smtplib
gh-badge: [star, fork, follow]
thumbnail-img: /assets/posts/python1-alini.png
share-img: /assets/posts/python1-alini.png
tags: [python, tutorial]
---
![pythonlini1](/assets/posts/python1-alini.png){: .mx-auto.d-block :}

Estes dias pesquisei qual a forma mais simples de enviar emails com anexos, utilizando Python e vim compartilhar o que encontrei.

Para enviar um email a partir de uma aplicação, precisamos seguir o protocolo SMTP, (Simple Mail Transfer Protocol). Hoje todas nossas atividades na internet são possíveis porque existem protocolos, que são regras e diretrizes do software de rede que permitem que um computador se conecte a redes em qualquer lugar. 

Para iniciar nossa aplicação, precisamos nos conectar a um servidor SMTP, que é um é um computador que recebe os emails e os entrega a seus respectivos destinatários.
Como vamos utilizar o servidor smtp da Google, precisamos gerar uma senha para ser utilizada pela nossa aplicação: https://myaccount.google.com/apppasswords

![pythonlini12](/assets/posts/senha-google.png){: .mx-auto.d-block :}

A senha que será gerada, será utilizada para realizar login em nossa aplicação.

Em Python utilizamos o módulo smtplib, para utilizá-lo não precisamos fazer nenhuma instalação extra, pois ele é um módulo built-in.

Para a construção da nossa funcionalidade  precisamos seguir os seguintes passos:

- Montar o corpo do email;
- Adicionar anexo;
- Criar conexão com servidor SMTP;
- Fazer o login no servidor;
- Enviar o email.

Segue o código final do envio de email:
~~~

GOOGLE_SMTP = 'smtp.gmail.com'
GOOGLE_SMTP_PORT = 465
SMTP_LOGIN = 'seu_email@gmail.com'
SMTP_PASS = Senha gerada no passo anterior

// Monta o corpo do email
def get_body() -> MIMEMultipart:
message = MIMEMultipart()
message['From'] = f"Tutorial <{send_from}>"
message['To'] = send_to
message['Subject'] = subject

body = MIMEText(text)
message.attach(body)

return message


// Adiciona o anexo ao Email
def add_attachment(message: MIMEMultipart) -> MIMEMultipart:
with open(file_name) as fp:
record = MIMEText(fp.read())
record['Content-Disposition'] = 'attachment; filename="test.csv"'
message.attach(record)
return message


// Envia o email
def send_email(message: MIMEMultipart):
server = smtplib.SMTP_SSL(GOOGLE_SMTP, GOOGLE_SMTP_PORT)
server.login(SMTP_LOGIN, SMTP_PASS)
server.sendmail(send_from, send_to, message.as_string())
server.quit()


message = get_body()
message = add_attachment(message)
send_email(message)

~~~

E assim, com menos de 10 minutos, conseguimos enviar um email com anexo.
Para mais informações, você pode analisar a Documentação do Python.
O código está disponível em meu GitHub!

Abraço,
Alini!