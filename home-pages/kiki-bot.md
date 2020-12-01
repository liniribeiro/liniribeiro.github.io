---
layout: page
title: Kiki
subtitle: A primeira assistente de IA da Alini
---
![fotodaalini](/assets/img/chatbot/kiki-bot.png){: .alini-img .mx-auto.d-block :}

  <div class="container">
        <!--chatbot widget -->
        <div class="widget">
            <div class="chat_header">
                <!--Add the name of the bot here -->
                <span class="chat_header_title">
                <img class="chat_icon" src="/assets/img/icon-alini.png">Kiki
                <span class="dropdown-trigger" id="close">X</span>
                </span>    
            </div>
            <!--Chatbot contents goes here -->
            <div class="chats" id="chats">
                <div class="clearfix"></div>
            </div>
            <!--keypad for user to type the message -->
            <div class="keypad">
                <textarea id="userInput" placeholder="Type a message..." class="usrInput"></textarea>
                <div id="sendButton"><i class="fa fa-paper-plane" aria-hidden="true"></i></div>
            </div>
        </div>
        <!--bot profile-->
        <div class="profile_div" id="profile_div">
            <img class="imgProfile" src="/assets/img/chatbot/kiki-bot.png" />
        </div>
    </div>