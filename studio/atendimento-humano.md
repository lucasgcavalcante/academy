# Passando para um atendente humano

Use o bloco Atendimento humano para entregar a conversa à sua equipe, no grupo certo.

{% hint style="info" %}
Tempo de leitura: 5 min · Para quem: quem monta automações e gestores
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## Quando usar

Toda automação precisa de uma porta de saída para uma pessoa. Os casos mais comuns:

- O cliente escolhe "Falar com a equipe" num **Menu de opções**.
- O **Agente IA** reconhece uma intent como "Falar com atendente".
- O **Expediente** indica que a equipe está trabalhando.

Quando a conversa chega ao bloco **Atendimento humano**, a automação para de responder e a conversa passa para a equipe.

## Antes de começar

O bloco envia a conversa para um **grupo de atendimento**. Os grupos são criados pelo administrador em **Configurações** > **Grupos**. Veja como em [Grupos de atendimento](../administracao/grupos.md).

## Passo a passo

1. Na paleta, em **Saídas**, arraste **Atendimento humano** para o canvas.
2. Ligue a ele o caminho que deve chamar a equipe: a opção do menu, a intent do agente ou a saída **Dentro do expediente**.
3. Dê dois cliques no card (ou passe o mouse e clique em **Editar**). O painel **Atendimento humano** abre.
4. No campo **Time**, escolha o grupo que vai receber a conversa.
5. Clique em **Salvar**.

<!-- PRINT: painel "Atendimento humano" com o campo "Time" aberto, mostrando "Padrão da conexão", a lista de grupos e "Usar variável…" -->

O card mostra o grupo escolhido, por exemplo "Time: Financeiro".

{% hint style="info" %}
No bloco, o campo se chama **Time**. Ele lista os mesmos grupos que você vê em **Configurações** > **Grupos**.
{% endhint %}

## As opções do campo Time

- **Padrão da conexão**: usa o grupo padrão do canal por onde o cliente chegou. É a opção que já vem marcada.
- **Um grupo da lista**: a conversa sempre vai para esse grupo.
- **Usar variável…**: o grupo é decidido durante a conversa. Opção avançada, para quando um passo anterior do fluxo já guardou numa variável qual grupo deve atender.

Se nenhum grupo for definido, nem no bloco nem no canal, a conversa não se perde: ela vai para a espera geral do atendimento.

## Vários grupos no mesmo fluxo

Você pode usar quantos blocos **Atendimento humano** quiser, cada um com um grupo. Exemplo com um menu:

- "Segunda via de boleto" → **Atendimento humano** com o grupo Financeiro.
- "Problema com pedido" → **Atendimento humano** com o grupo Suporte.

<!-- PRINT: canvas com um Menu de opções cujas opções levam a dois blocos "Atendimento humano", um com "Time: Financeiro" e outro com "Time: Suporte" -->

## Depois da transferência

O bloco **Atendimento humano** não tem saída: o fluxo termina ali. A conversa aparece para os atendentes do grupo na tela de conversas, e eles seguem dali. Veja o lado do atendente em [Conhecendo a tela de conversas](../atendimento/tela-de-conversas.md).

{% hint style="warning" %}
Avise o cliente antes de transferir. Coloque um **Enviar Mensagem** antes do bloco, com algo como "Vou chamar alguém da equipe, só um instante." Assim ele não fica sem resposta enquanto espera.
{% endhint %}

## Próximos passos

Conecte outras ferramentas ao seu projeto: [Integrações do projeto](integracoes.md).
