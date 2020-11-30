---
layout: post
title: "Instalando Python"
subtitle: Passo a passo da instalação do Python
thumbnail-img: /assets/posts/instaling-python/Instalando-python-thum.png
share-img: /assets/posts/instaling-python/Instalando-python-thum.png
tags: [tutorial, python, instalation]
---
![pythonlini1](/assets/posts/instaling-python/Instalando-python.png){: .mx-auto.d-block :}

Para unificar todos os conteúdos em apenas uma página, trouxe um passo a passo da instalação do Python, separado por sistema operacional:

![install-python-windows](/assets/posts/instaling-python/windows.png){: .post-http-small-image :}
## Instalando o Python no Windows

O primeiro passo é acessar o site do Python: https://www.python.org/.
Na sessão de Downloads, automaticamente já será disponibilizado o instalador específico do Windows, portanto é só baixar o Python 3, na sua versão mais atual.

![install-python1](/assets/posts/instaling-python/installpython1.png){: .mx-auto.d-block :}

Ou podemos escolher uma versão específica a partir deste [Link](https://www.python.org/downloads/windows/)
![install-python1](/assets/posts/instaling-python/python-install.gif){: .mx-auto.d-block :}

Após o download ser finalizado, abra-o e logo na primeira tela é importante marcar a checkbox **Add Python 3.8 to PATH**. 
Essa opção é importante para conseguirmos executar o Python dentro do Prompt de Comando do Windows.

![install-python2](/assets/posts/instaling-python/installpython2.png){: .mx-auto.d-block :}

Vamos selecionar a opção “Install Now” e aguardar o término da instalação.

![install-python3](/assets/posts/instaling-python/installpython3.png){: .mx-auto.d-block :}

#### Testando o Python

Terminada a instalação, podemos testar se o Python foi instalado corretamente. Podemos abrir o Prompt de Comando e executar o seguinte comando:
~~~~
	python - V
~~~~

![install-python4](/assets/posts/instaling-python/installpython4.png){: .mx-auto.d-block :}

<br>

## Instalando Python em outras plataformas

![install-python-linux](/assets/posts/instaling-python/linux.png){: .post-http-small-image :}

Os sistemas operacionais baseados no Debian já possuem o Python 3 pré-instalado, mas o comandos para instalá-lo pelo terminal é:
~~~~
sudo apt-get update
sudo apt-get install python3
~~~~

Assim como no Windows, você pode verificar se o Python 3 está instalado executando o seguinte comando:
~~~~
python3 -V
~~~~
E para executar o Python 3, basta rodar o comando python3 no terminal.

<br>
<br>

## Instalando o Python no MacOS

![install-python-macos](/assets/posts/instaling-python/macos.png){: .post-http-small-image :}
Para instalar o Python 3 no MacOS, temos duas opções, através do Homebrew, fazemos:
~~~~
brew update
brew install python3
~~~~
Mas caso você não utiliza o Homebrew, podemos baixar o instalador do Python através do seu site oficial. Assim como no Windows, na sessão de Downloads, o site automaticamente já detectará o seu sistema operacional e disponibilizará o instalador específico para o seu MacOS, portanto é só baixar o Python 3, na sua versão mais atual.
E assim como nos sistemas baseados no Debian, verificamos a versão do Python com o seguinte comando:
~~~~
python3 -V
~~~~
E o executamos rodando o comando **python3** no terminal.


## IDE Pycharm

Para realizar o download da IDE que será utilizada para a construções de nossos projetos, basta entrar na página da Jetbrains e realizzar o download da versão **Community** e seguir com a instalação:

[Página para o download do Pycharm](https://www.jetbrains.com/pycharm/download/#section=windows)

Em breve iremos construir o esqueleto de um projeto para iniciar nossa aventura com o Python!



Passos simples não é mesmo?? 
<br>
Vamos codar agora? ❤️

Grande Abraço, A.R. 🙂
