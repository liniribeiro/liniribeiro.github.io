---
layout: post
title: Utilizando toasts em seu app Android
subtitle: Passo a passo da utilização de Toasts em um app Android!
gh-repo: liniribeiro/yourselfCoffeeShop
gh-badge: [star, fork, follow]
thumbnail-img: /assets/posts/toast-alini-ribeiro.png
share-img: /assets/posts/toast-alini-ribeiro.png
tags: [android, tutorial]
---
![toastlini1](/assets/posts/toast-alini-ribeiro.png){: .mx-auto.d-block :}

Estou fazendo um curso super legal na Udacity de Android. Um dos capítulos, nos indica a ler a documentação sobre mensagens Toasts, que são uma forma rápida de falar algo para o usuário, um pop-up rapidinho que mostra a mensagem e some em dois ou quatro segundos (conforme a configuração realizada). Como adoro escrever para fixar conhecimento e também compartilhar um pouquinho do que eu estudo segue um tutorial rápidinho de, como utilizar toasts em um app Android.


### Criando uma Toast básica


Usamos o método makeText() que possui três parâmetros:
- O contexto que é normalmente da application ou da activity;
- A mensagem que é a mensagem que será mostrada no toast;
- A duração que o pop-up ficará visível.

Na duração, temos duas opções, LENGTH_SHORT que é em torno de dois segundos, ou LENGTH_LONG que fica aparecendo a mensagem por volta de 4 segundos.

Exemplo:
~~~
Context context = getApplicationContext();
CharSequence messagem = "Eu gosto de torrada torrada";
final Toast toastBasic = Toast.makeText(context, message, Toast.LENGTH_SHORT);
~~~

Para ver a sua Toast, é só chamar com o método show():
~~~
toastBasic.Show();
~~~

Ou fazer tudo direto:
~~~
Toast.makeText(this, "Eu gosto de torrada torrada", Toast.LENGTH_SHORT).show();
~~~

<br>
### Posição do toast

Podemos colocar nossa toast em qualquer lugar da tela, onde você prefere?
A posição padrão é centralizado na parte inferior da tela, para altera-lá  utilizamos o método setGravity(). Este método seta a posição da nossa Toast na tela e possui três parâmetros:
- Gravity: Especifica o posicionamento da Toast na tela;
- xOffset: Alterando este valor, ele move a Toast para a direita e esquerda;
- yOffset: Alterando este valor, ele move a Toast para cima e para baixo.

~~~
Context context = getApplicationContext();
CharSequence messagem = "Eu gosto de torrada torrada";
int duration = Toast.LENGTH_SHORT;

int MoveToastDown = 150;
int movetoastRight = 150;

final Toast toastTop = Toast.makeText(context, message, duration);
toastTop.setGravity(Gravity.TOP | Gravity.LEFT, movetoastRight, MoveToastDown);
toastTop.Show();
~~~

<br>
### Customizando a toast


Para uma Toast diferentona, precisamos criar um layout e salvar na pasta  res/layout como um arquivo xml (toast_layout.xml).
Precisamos criar uma view e inflar o layout que criamos, criar uma toast com apenas o contexto de parâmetro, e setar a nossa view no Toast:

Exemplo:
~~~
LayoutInflater inflater = getlayoutinflater();

//infla o layout na view
View view = inflater.inflate(R.Layout.toast_layout, (ViewGroup)findViewById(R.id.custom.toasty.container));

//Cria um TextView para mostrar o texto do Toast
TextView text = (TextView) view.findViewbyId(R.id.text);

//Informa o texto para ser exibido
text.settext(getString(R.string.custom_toast_text));

//Cria o toast
final Toast customToast = new Toast(context);

//informa a posição
customToast.setGravity(Gravity.CENTER_VERTICAL, 0, 0);

//informa o tempo que o Toast ficará visível
customToast.setDuration(Toast.LENGTH_LONG);

//informa a view que o toast vai usar
customToast.setView(view);

//mostra a Toast
customToast.Show();
~~~


Você pode acessar um código com estes exemplos em meu Github.

Grande Abraço,
Alini!