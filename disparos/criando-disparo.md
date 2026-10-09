# Criando um disparo passo a passo

Envie um template aprovado para vários contatos de uma vez, agora ou em data marcada.

{% hint style="info" %}
Tempo de leitura: 7 min · Para quem: gestores
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## Antes de começar

- Tenha um template **Aprovado** na conexão que vai enviar. Veja [Criando um template](../templates/criando-template.md).
- Tenha o público em mente. Veja [Preparando o público do disparo](preparando-o-publico.md).
- Para ver o item no menu, seu usuário precisa ser administrador ou ter um cargo com a permissão **Gerenciar disparos**.

## Abrindo o assistente

1. No menu lateral, clique no ícone de avião de papel. O nome do item aparece como **Campanhas**.
2. A tela **Disparos** abre. Clique em **Novo disparo**.

O assistente tem cinco etapas: **Configuração**, **Mensagem**, **Público**, **Envio** e **Revisão**. Use **Continuar** para avançar e **Voltar** para corrigir algo. Se faltar alguma informação, o assistente avisa e não avança.

<!-- PRINT: topo do assistente "Novo disparo" mostrando as cinco etapas -->

## 1. Configuração

1. Em **Nome do disparo**, dê um nome que facilite achar depois, como "Black Friday — Clientes VIP". Só você e sua equipe veem esse nome.
2. Em **Conexão**, clique na conexão que vai enviar. As conexões do WhatsApp Oficial aparecem com a indicação "Business API".

{% hint style="warning" %}
Se você trocar a conexão depois de escolher o template, o template escolhido é desmarcado. Templates pertencem a uma conexão.
{% endhint %}

## 2. Mensagem

1. Escolha um dos templates da lista. Só aparecem templates **Aprovados** da conexão escolhida.
2. Confira a **PRÉVIA** à direita.

Se o template tem variáveis, uma nota avisa quantas são. Você define os valores na etapa seguinte.

Se a lista estiver vazia, aparece "Nenhum template aprovado para esta conexão." e o botão **Gerenciar templates**, que abre a tela de templates em outra aba.

<!-- PRINT: etapa Mensagem com um template selecionado e a prévia do WhatsApp à direita -->

## 3. Público

Escolha **Contatos da agenda** ou **Importar planilha CSV** e defina os destinatários. Todos os detalhes estão em [Preparando o público do disparo](preparando-o-publico.md).

## 4. Envio

### Quando enviar

- **Agora**: o disparo começa assim que você confirmar.
- **Agendar**: escolha a data e o horário. A data precisa estar no futuro.

### Ritmo de envio

O ritmo define o intervalo entre uma mensagem e a próxima.

- **Fixo**: o mesmo intervalo entre todas as mensagens. Ajuste na barra ou digite os segundos. O padrão é 20 segundos.
- **Aleatório**: um intervalo que varia **entre** um mínimo e um máximo, em segundos. O padrão é de 5 a 25. O máximo precisa ser maior que o mínimo.

Quanto maior o intervalo, mais tempo o disparo leva para terminar. Um disparo para 300 contatos com intervalo fixo de 20 segundos leva cerca de 1 hora e 40 minutos.

{% hint style="warning" %}
Intervalos menores que 10 segundos geram um alerta. Envios muito rápidos aumentam o risco de problemas com o WhatsApp.
{% endhint %}

### Fluxo de saída

Defina para onde vão as respostas dos contatos:

- **Nenhum — respostas vão para a fila**: as respostas chegam para a equipe na tela de conversas.
- Um fluxo do **Studio**: as respostas são tratadas pelo fluxo escolhido. Veja [Conhecendo o Studio](../studio/conhecendo-o-studio.md).

<!-- PRINT: etapa Envio com "Agendar" selecionado, data e horário preenchidos, ritmo "Aleatório" e o campo "Fluxo de saída" -->

## 5. Revisão

Confira o resumo em três blocos:

- **Configuração**: nome e conexão.
- **Mensagem**: template, categoria, idioma e de onde vem cada variável.
- **Envio**: início, ritmo e fluxo de saída.

À direita ficam a prévia e o total de destinatários.

Tudo certo? Clique em **Lançar disparo**. Você volta para a tela **Disparos**, onde o novo disparo aparece como **Enviando** ou **Agendado**.

<!-- PRINT: etapa Revisão com os três blocos preenchidos e o botão "Lançar disparo" -->

{% hint style="success" %}
Antes de um envio grande, faça um disparo de teste para você e para alguém da equipe. Assim você confere a mensagem como o cliente vai receber.
{% endhint %}

## Editando, cancelando e excluindo

Na tela **Disparos**, use o menu de ações (⋯) no fim da linha do disparo:

- **Editar**: reabre o assistente com os dados do disparo. Ao final, clique em **Salvar disparo**.
- **Cancelar envio**: interrompe um disparo **Agendado** ou **Enviando**.
- **Excluir**: apaga o disparo. Esta ação não pode ser revertida.

## Próximos passos

Veja como acompanhar os envios: [Acompanhando o relatório do disparo](relatorio-do-disparo.md).
