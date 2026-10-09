# Os blocos do fluxo

Conheça cada bloco da paleta do editor e saiba quando usar cada um.

{% hint style="info" %}
Tempo de leitura: 9 min · Para quem: quem monta automações
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## Como a paleta funciona

A paleta fica à esquerda do editor. Os blocos estão separados em cinco categorias: **Conversa**, **Agente de IA**, **Ferramentas**, **Lógica** e **Saídas**. Clique no nome de uma categoria para recolher ou abrir.

- Use **Buscar bloco** para achar um bloco pelo nome.
- Passe o mouse sobre um bloco para ver a descrição.
- Arraste o bloco para o canvas ou para dentro de um grupo.

<!-- PRINT: paleta de blocos com as cinco categorias abertas e o campo "Buscar bloco" no topo -->

### Grupos e blocos soltos

Existem dois tipos de bloco no canvas:

- **Itens de grupo**: ao soltar no canvas, viram um card chamado grupo. Você pode empilhar vários itens no mesmo grupo, e eles rodam de cima para baixo. Depois do último item, o fluxo segue pela saída do grupo (a bolinha na borda direita do card). Para renomear o grupo, clique no título dele.
- **Blocos soltos**: ficam sozinhos no canvas, num card próprio. São o **Agente IA**, o **Expediente** e os blocos de **Saídas**.

Para editar um item de grupo, clique nele. O **Agente IA** e o **Atendimento humano** abrem com dois cliques no card ou pelo botão **Editar**, que aparece quando você passa o mouse. O **Expediente** e o **Redirecionar** são configurados direto no card. Para remover qualquer bloco, passe o mouse e clique em **Excluir**.

{% hint style="warning" %}
No painel de edição, fechar o painel (pelo **X**, por **Cancelar**, pela tecla Esc ou clicando fora) também guarda o que você escreveu. **Cancelar** não desfaz as alterações.
{% endhint %}

### O que é uma variável

Vários blocos falam em **variável**. Pense numa caixinha com nome que guarda uma informação durante a conversa, como o nome do cliente ou o número de um pedido.

Para usar o conteúdo de uma variável num texto, escreva o nome dela entre chaves duplas, por exemplo `{{nomeCliente}}`. Ao digitar `{{`, o editor sugere as variáveis que existem. Se aparecer um sinal de alerta no nome, a variável não existe no projeto.

As variáveis do projeto ficam na engrenagem **Configurações do projeto**, em **Variáveis** > **Nova variável**. Você também pode criar uma na hora, pela opção **Criar nova variável...** nos campos de variável.

## Conversa

Blocos que falam com o cliente ou esperam a resposta dele.

### Enviar Mensagem

Envia uma mensagem para o cliente. Você pode:

- Escrever o texto e usar variáveis, como `{{nomeCliente}}`.
- Anexar uma imagem, vídeo, áudio ou documento pelo clipe (**Anexar mídia**), até 50 MB.

{% hint style="info" %}
O ícone de chaves (**Editar como JSON (avançado)**) é para usos técnicos. Se você não sabe o que é, pode ignorar.
{% endhint %}

### Menu de opções

Mostra uma pergunta com opções para o cliente escolher. Cada opção vira uma saída própria, que você liga ao próximo passo.

- **Mensagem**: a pergunta.
- **Opções do menu**: as escolhas. Use **Adicionar opção** para incluir mais.

Em **Opções avançadas** você define o que acontece quando o cliente não responde direito:

- **Tentativas inválidas permitidas**: quantas respostas fora das opções o menu aceita antes de desistir. Com mais de 0, você pode ligar **Criar saída “Tentativas excedidas”**.
- **Mensagem de tentativa**: o aviso enviado antes de mostrar o menu de novo.
- **Tratar quando não houver resposta**: quantos minutos esperar. Você pode ligar **Criar saída “Sem resposta”**.

Sem essas saídas extras, o fluxo continua no próximo item do grupo.

<!-- PRINT: item "Menu de opções" no canvas com três opções, cada uma com sua bolinha de saída à direita -->

### Entrada do usuário

Pausa o fluxo e espera a próxima mensagem do cliente. A resposta fica guardada numa variável, escolhida em **Salvar resposta em**.

Use para perguntas abertas, como "Qual é o seu e-mail?". Com **Timeout se não responder**, você define quantos minutos esperar e pode criar a saída **Sem resposta**.

## Agente de IA

### Agente IA

Coloca uma IA para conversar com o cliente, seguindo as instruções que você escrever e consultando as bases de conhecimento do projeto. Tem uma aula só para ele: [Agente de IA e base de conhecimento](agente-de-ia.md).

## Ferramentas

Blocos que buscam ou enviam informações para outros sistemas.

### Google Agenda, Google Sheets e Shopify

Cada ferramenta tem seu bloco:

- **Google Agenda**: consultar eventos, verificar disponibilidade e criar eventos.
- **Google Sheets**: adicionar, buscar e atualizar linhas em uma planilha.
- **Shopify**: consultar pedidos e produtos de uma loja.

Ao editar, você escolhe a **Conta conectada**, depois a **Ação** e preenche os campos dela. Se ainda não houver conta, o próprio bloco oferece o botão para conectar. Veja mais em [Integrações do projeto](integracoes.md).

### HTTP Request

Conversa com outros sistemas pela internet (uma API). É um bloco para quem já tem os dados técnicos do sistema que vai chamar: endereço, método e, se for o caso, o corpo da requisição. A resposta pode ser guardada em variáveis.

{% hint style="info" %}
Para chaves de acesso e senhas, use os **Secrets** das **Configurações do projeto**, em vez de colar a chave direto no bloco.
{% endhint %}

## Lógica

Blocos que decidem o caminho do fluxo ou preparam informações.

### Expediente

Divide o fluxo em dois caminhos: **Dentro do expediente** e **Fora do expediente**. Escolha um expediente cadastrado no próprio card, em **Selecione um expediente**, ou crie um com **Criar novo expediente**.

Exemplo: dentro do horário, a conversa vai para a equipe; fora dele, o cliente recebe um aviso com o horário de atendimento.

### Condição

Escolhe o caminho a partir de regras. Cada regra tem um nome e vira uma saída.

1. Dê um nome para a saída (por exemplo, "Cliente VIP").
2. Monte a regra: a variável, a comparação (**é igual a**, **contém**, **maior que**, **está vazio** e outras) e o valor.
3. Use **Adicionar condição** para juntar mais de uma comparação na mesma regra. Aí você escolhe se precisam valer **todas (E)** ou **qualquer (OU)**.
4. Use **Adicionar saída** para criar outra regra, com outro caminho.

Se nenhuma regra servir, o fluxo segue pela saída do grupo. Funciona como o "senão".

### Executar

Roda um pequeno código em JavaScript para transformar informações. É um bloco para quem programa. Se esse não for o seu caso, prefira **Definir Variável** e **Condição**.

### Definir Variável

Guarda um valor numa variável. Escolha a variável em **Nome da variável** e escreva o **Valor**. O valor pode usar outras variáveis.

Exemplo: guardar "sim" em `{{querOrcamento}}` quando o cliente escolhe "Pedir orçamento" no menu, para usar numa **Condição** mais adiante.

## Saídas

Blocos que encerram a parte automática ou mandam a conversa para outro lugar. Eles não têm saída: depois deles, o fluxo atual termina.

### Atendimento humano

Passa a conversa para a equipe, no grupo de atendimento que você escolher. Detalhes em [Passando para um atendente humano](atendimento-humano.md).

### Finalizar conversa

Encerra a conversa. Não tem configuração.

### Redirecionar

Leva a conversa para outro fluxo do mesmo projeto. Escolha o fluxo em **Redirecionar para**. As variáveis da conversa continuam valendo no fluxo de destino.

Use para separar assuntos em fluxos menores, como "Financeiro" e "Suporte", em vez de montar tudo num fluxo só.

{% hint style="warning" %}
Um fluxo que é destino de um **Redirecionar** não pode ser excluído enquanto estiver sendo usado.
{% endhint %}

## Comentários no canvas

Clique com o botão direito no canvas e escolha **Adicionar comentário** para deixar uma anotação para a equipe. Comentários não afetam o fluxo.

## Próximos passos

Coloque uma IA para conversar no seu fluxo: [Agente de IA e base de conhecimento](agente-de-ia.md).
