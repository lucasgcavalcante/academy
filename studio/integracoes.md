# Integrações do projeto

Conecte contas externas, como Google Agenda, Google Sheets e Shopify, para usar nos fluxos e no agente de IA.

{% hint style="info" %}
Tempo de leitura: 5 min · Para quem: gestores e quem monta automações
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## O que são as integrações

Integrações são contas de outros sistemas que o seu projeto pode usar. Com elas, a automação faz coisas como marcar um horário na agenda, registrar um pedido numa planilha ou consultar o status de uma compra.

Cada projeto tem as suas integrações. Se você usar a mesma conta em dois projetos, precisa conectá-la em cada um.

## Abrindo a página

Você chega lá de dois jeitos:

- No editor, em **Recursos do projeto** (rodapé da paleta), clique em **Integrações**. O editor salva o fluxo antes de sair.
- Na barra lateral do projeto, clique em **Integrações**.

<!-- PRINT: página "Integrações" do projeto, com a seção "Disponíveis" e a seção "Contas conectadas neste projeto" -->

A página tem duas partes:

- **Disponíveis**: as integrações que o projeto pode conectar, com quantas contas cada uma já tem. Hoje são **Google Agenda**, **Google Sheets** e **Shopify**. O **Jira** aparece como **em breve**.
- **Contas conectadas neste projeto**: as contas já conectadas e a situação de cada uma.

{% hint style="warning" %}
Somente administradores podem conectar, reconectar ou desconectar contas nesta página.
{% endhint %}

## Conectando uma conta

### Google Agenda e Google Sheets

1. Em **Disponíveis**, clique em **Conectar** na integração.
2. Você vai para a página do Google. Entre com a conta que quer usar e autorize o acesso.
3. Ao terminar, você volta para a página de Integrações, com a conta em **Contas conectadas neste projeto**.

### Shopify

1. Em **Disponíveis**, clique em **Conectar** na linha do Shopify.
2. Informe o **Domínio da loja**, no formato `minhaloja.myshopify.com`.
3. Clique em **Continuar** e autorize o acesso na sua loja.

## A situação de cada conta

Em **Contas conectadas neste projeto**, cada conta mostra:

- **Conectada**: tudo certo.
- **Reconectar**: o acesso expirou ou foi revogado. Clique em **Reconectar** e autorize de novo.
- **Desconectada**: a conta foi desconectada e não pode ser usada.

Para tirar uma conta do projeto, clique em **Desconectar** e confirme.

{% hint style="warning" %}
Ao desconectar, os blocos e ferramentas do projeto que usam essa conta param de funcionar até você conectar uma conta de novo. Desconectar apaga o acesso guardado no Revodesk, mas não remove a autorização no Google ou no Shopify. Se quiser remover por lá, faça isso no painel da própria ferramenta.
{% endhint %}

## Usando a integração no fluxo

Existem dois jeitos de usar uma conta conectada.

### Como bloco do fluxo

Use quando a ação deve acontecer sempre naquele ponto do fluxo, como registrar um pedido na planilha.

1. Na paleta, em **Ferramentas**, arraste o bloco da integração (por exemplo, **Google Sheets**).
2. Clique no item para editar.
3. Em **Conta conectada**, escolha a conta.
4. Em **Ação**, escolha o que o bloco deve fazer.
5. Preencha os campos da ação e salve.

Se ainda não houver conta, o bloco mostra o botão **Conectar** com o nome da integração, e você conecta dali mesmo.

<!-- PRINT: painel de um bloco Google Sheets com os campos "Conta conectada" e "Ação" preenchidos -->

### Como ferramenta do agente de IA

Use quando o agente deve decidir sozinho, durante a conversa, a hora de agir. Por exemplo, consultar horários livres na agenda quando o cliente pede para marcar.

No painel do **Agente IA**, em **Ferramentas**, clique em **Adicionar** e escolha a ação. Veja o passo a passo em [Agente de IA e base de conhecimento](agente-de-ia.md).

{% hint style="success" %}
No painel de teste, ações que alteram dados (como criar um evento ou adicionar uma linha) só acontecem de verdade quando a opção **Permitir ações reais neste teste (administrador)** está marcada.
{% endhint %}

## Próximos passos

Você terminou a trilha do Studio. Para colocar seu projeto para atender, ligue-o a um canal: [Conectando seus canais](../administracao/conectando-canais.md).
