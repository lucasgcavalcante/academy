# Configurações da empresa

Conheça a tela de Configurações e ajuste a avaliação do atendimento e as regras de inatividade.

{% hint style="info" %}
Tempo de leitura: 5 min · Para quem: gestores (administradores)
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## A tela de Configurações

No menu lateral, clique em **Configurações** (ícone de engrenagem, na parte de baixo). A tela reúne os ajustes da empresa em três grupos. Cada pessoa vê só os itens que o acesso dela permite.

**Atendimento**

| Item | Onde aprender |
| --- | --- |
| **Canais de atendimento** | [Conectando seus canais](conectando-canais.md) |
| **Atendentes** | [Usuários, cargos e permissões](usuarios-e-cargos.md) |
| **Grupos** | [Grupos de atendimento](grupos.md) |
| **Cargos personalizados** | [Usuários, cargos e permissões](usuarios-e-cargos.md) |
| **Etiquetas** | [Organizando com etiquetas](../contatos/etiquetas.md) |
| **Campos personalizados** | [Campos personalizados](../contatos/campos-personalizados.md) |

**Automação**

| Item | Onde aprender |
| --- | --- |
| **Modelos de mensagens** | [Criando um template](../templates/criando-template.md) |
| **Chatbots** | [Conhecendo o Studio](../studio/conhecendo-o-studio.md) |

**Organização**

| Item | O que tem |
| --- | --- |
| **Configurações gerais** | Avaliação do atendimento e regras de inatividade. Veja abaixo. |
| **Financeiro** | Dados de pagamento, faturas e cartões cadastrados. Só administradores veem. |

<!-- PRINT: tela Configurações completa, vista por um administrador, com os grupos Atendimento, Automação e Organização -->

## Configurações gerais

Em **Configurações**, clique em **Configurações gerais**. A tela tem três abas: **Avaliações**, **Mensagens rápidas** e **Regras de inatividade**.

### Avaliações

Em **Avaliação do atendimento**, ligue ou desligue **Solicitar avaliação**.

Com a opção ligada, quando a conversa é encerrada, o contato recebe um pedido de nota de 1 a 5. Ele tem 15 minutos para responder.

A mudança vale na hora, sem botão de salvar.

<!-- PRINT: aba Avaliações com o interruptor "Solicitar avaliação" ligado -->

### Mensagens rápidas

Esta aba ainda não tem opções. As respostas rápidas usadas nas conversas são explicadas em [Respostas rápidas com /](../atendimento/respostas-rapidas.md).

### Regras de inatividade

Defina o que acontece quando o contato para de responder. O tempo é contado a partir da última mensagem enviada pelo atendente.

1. No cartão **Contato inativo**, ligue **Ativar**.
2. Em **Ação automática**, escolha:
   - **Fechar conversa**: fecha a conversa depois do tempo definido.
   - **Avisar e fechar**: manda um lembrete e, se o contato continuar sem responder, fecha a conversa.
   - **Apenas avisar**: só manda o lembrete.
3. Preencha os tempos, em minutos (de 1 a 1.440, ou seja, até 24 horas):
   - **Tempo para enviar aviso (minutos)**: quanto tempo sem resposta até o lembrete.
   - **Tempo para fechar conversa (minutos)**: quanto tempo sem resposta até fechar. Em **Avisar e fechar**, ele precisa ser maior que o tempo do aviso.
4. Escreva as mensagens:
   - **Mensagem de aviso**: o lembrete enviado ao contato.
   - **Mensagem de encerramento**: enviada quando a conversa é fechada por inatividade.
5. Clique em **Salvar**.

Os campos mudam conforme a ação escolhida. Em **Fechar conversa**, por exemplo, não há tempo nem mensagem de aviso.

<!-- PRINT: aba Regras de inatividade com "Avisar e fechar" selecionado, os dois tempos e as duas mensagens preenchidos -->

{% hint style="success" %}
Exemplo: aviso em 30 minutos e fechamento em 60. Se o contato não responder em 30 minutos, recebe o lembrete. Se continuar sem responder até 60 minutos, a conversa é fechada com a mensagem de encerramento.
{% endhint %}

{% hint style="warning" %}
No WhatsApp, a janela de 24 horas também vale para essas mensagens automáticas. Veja [O que são templates e a janela de 24 horas](../templates/o-que-sao-templates.md).
{% endhint %}

O cartão **Atendente inativo** aparece marcado como "Em breve" e ainda não tem opções.

## Próximos passos

Você concluiu a trilha de Administração. Volte ao início da Revo Academy para rever qualquer tema: [Boas-vindas à Revo Academy](../README.md).
