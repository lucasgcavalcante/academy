# Montando seu primeiro fluxo

Crie um projeto, monte um fluxo simples de boas-vindas, teste e publique.

{% hint style="info" %}
Tempo de leitura: 7 min · Para quem: quem monta automações
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## O que você vai montar

Um fluxo curto: o cliente manda uma mensagem, recebe uma saudação e escolhe entre duas opções num menu. Com isso você pratica tudo o que vai usar no dia a dia: arrastar blocos, ligar um ao outro, testar e publicar.

## 1. Crie o projeto

1. Clique em **Studio** no menu lateral.
2. Clique em **Novo projeto**.
3. Preencha o **Nome** (por exemplo, "Atendimento da loja"). A **Descrição** é opcional.
4. Clique em **Criar projeto**.

<!-- PRINT: janela "Novo projeto" com os campos Nome e Descrição preenchidos e o botão "Criar projeto" -->

O projeto aparece na lista. Ele já nasce com um fluxo de entrada, chamado "*nome do projeto* - Atendimento principal".

## 2. Abra o editor

Clique no nome do projeto na lista. O editor abre no fluxo de entrada, com o bloco **Início** no canvas. Toda conversa começa por ele.

{% hint style="info" %}
O bloco **Início** não pode ser excluído. Ele só tem uma saída: a bolinha na borda direita.
{% endhint %}

## 3. Adicione uma mensagem

1. Na paleta, em **Conversa**, encontre **Enviar Mensagem**.
2. Arraste o bloco e solte no canvas, à direita do **Início**.
3. Um card novo aparece, com o item **Enviar Mensagem** dentro.
4. Clique no item para abrir o painel de edição.
5. Escreva a mensagem, por exemplo: "Olá! Bem-vindo à nossa loja."
6. Clique em **Salvar**.

<!-- PRINT: painel lateral "Enviar Mensagem" aberto, com o texto da mensagem escrito e o botão "Salvar" -->

{% hint style="info" %}
Muitos blocos viram um **grupo** quando você os solta no canvas: um card que guarda uma sequência de itens. Você pode arrastar outros blocos para dentro do mesmo grupo, onde aparece o aviso **Arraste blocos aqui**. Os itens rodam de cima para baixo.
{% endhint %}

## 4. Adicione um menu

1. Arraste **Menu de opções** para dentro do mesmo grupo, logo abaixo da mensagem.
2. Clique no item para editar.
3. Em **Mensagem**, escreva a pergunta: "Como podemos ajudar?"
4. Em **Opções do menu**, troque "Opção 1" e "Opção 2" por "Ver produtos" e "Falar com a equipe". Use **Adicionar opção** se precisar de mais.
5. Clique em **Salvar**.

Cada opção do menu ganha sua própria saída, uma bolinha à direita da linha da opção.

## 5. Conecte os blocos

1. Clique na bolinha à direita do **Início** e arraste até o card do grupo.
2. Solte. Uma seta liga os dois.
3. Para cada opção do menu, arraste da bolinha da opção até o bloco que deve vir depois. Para "Falar com a equipe", por exemplo, use o bloco **Atendimento humano**, que você conhece na aula [Passando para um atendente humano](atendimento-humano.md).

<!-- PRINT: canvas com Início ligado ao grupo (mensagem + menu) e a opção "Falar com a equipe" ligada a um bloco Atendimento humano -->

Para remover uma ligação, passe o mouse sobre a seta e clique na lixeira (**Remover conexão**).

## 6. Salve

Não existe botão de salvar: o editor salva sozinho. Acompanhe na barra do topo: **Salvando…** e depois **Salvo**.

O que fica salvo é um **rascunho**. O cliente só vê as mudanças depois que você publica.

{% hint style="warning" %}
O editor ainda não tem "desfazer". Se excluir um bloco por engano, você precisa montá-lo de novo.
{% endhint %}

## 7. Teste

1. Clique em **Testar** na barra do topo. O painel **Teste do fluxo** abre ao lado do canvas.
2. Clique em **Testar com “Olá”** ou escreva sua própria mensagem.
3. Converse como se fosse o cliente. No menu, clique numa opção para escolher.
4. Para começar de novo, use **Reiniciar teste**. Para sair, clique em **Fechar teste**.

<!-- PRINT: painel "Teste do fluxo" com a conversa de teste, mostrando a saudação e os botões das opções do menu -->

O teste usa o que está no canvas agora, mesmo sem publicar. A aba **Logs** mostra as consultas e ações feitas durante o teste.

{% hint style="warning" %}
A opção **Permitir ações reais neste teste (administrador)** faz as integrações agirem de verdade (por exemplo, criar um evento na agenda). Deixe desmarcada enquanto estiver só experimentando.
{% endhint %}

## 8. Publique

1. Clique em **Publicar**.
2. O Revodesk confere todos os fluxos do projeto que têm alterações. Se tudo estiver certo, aparece a confirmação de que os fluxos foram publicados e o selo muda para **Publicado**.
3. Se algum fluxo tiver problema, nada vai ao ar. A mensagem começa com **Não publicado** e mostra qual fluxo precisa de ajuste e o motivo.

Se não houver nada novo, o botão **Publicar** fica desabilitado.

## 9. Coloque o projeto para atender

Publicar deixa o fluxo pronto, mas ele só atende quando está ligado a um canal. Quem faz isso é o administrador, em **Configurações** > **Canais de atendimento**: no menu da conexão, **Configurar bot**, escolha o projeto e clique em **Salvar**. O passo a passo está em [Conectando seus canais](../administracao/conectando-canais.md).

{% hint style="success" %}
Pronto! Você criou, testou e publicou seu primeiro fluxo.
{% endhint %}

## Próximos passos

Conheça todos os blocos disponíveis e o que cada um faz: [Os blocos do fluxo](blocos-do-fluxo.md).
