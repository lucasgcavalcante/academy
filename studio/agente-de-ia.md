# Agente de IA e base de conhecimento

Coloque uma IA para conversar com seus clientes, usando o que a sua empresa sabe.

{% hint style="info" %}
Tempo de leitura: 9 min · Para quem: quem monta automações
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## Como funciona

O bloco **Agente IA** conversa com o cliente seguindo as instruções que você escreve. Ele responde mensagem após mensagem até reconhecer uma das **intents** (intenções) que você cadastrou, como "quer falar com um atendente". Nesse momento, a conversa sai do agente pelo caminho daquela intent.

Para responder bem sobre a sua empresa, o agente consulta a **base de conhecimento** do projeto: textos e arquivos com as informações que você quer que ele saiba.

A ordem recomendada é:

1. Montar a base de conhecimento.
2. Adicionar o agente no fluxo e escolher as bases que ele consulta.
3. Cadastrar as intents e ligar cada uma ao próximo passo.
4. Testar.

## 1. Monte a base de conhecimento

### Crie a base

1. No editor, em **Recursos do projeto** (rodapé da paleta), clique em **Base de conhecimento**. O editor salva o fluxo antes de sair.
2. Clique em **Nova base**.
3. Preencha o **Nome** (por exemplo, "Perguntas frequentes") e, se quiser, a **Descrição**.
4. Clique em **Criar base**. A base abre em seguida.

<!-- PRINT: página "Base de conhecimento" do projeto, com a lista de bases e os botões "Testar uma pergunta" e "Nova base" -->

### Ensine o conteúdo

Dentro da base, na área **Ensine algo novo para seus agentes**, você tem dois caminhos:

- **Arquivo**: envie PDF com texto, DOCX, TXT ou Markdown. São até 5 arquivos por vez, de até 50 MB cada. Você também pode arrastar os arquivos para essa área.
- **Texto**: escreva ou cole o conteúdo direto. Dê um **Nome** e preencha o **Conteúdo**, como perguntas frequentes, informações sobre produtos ou políticas.

<!-- PRINT: tela de uma base aberta, com a área "Ensine algo novo para seus agentes", os botões "Arquivo" e "Texto" e a lista de fontes abaixo -->

Cada item que você adiciona vira uma **fonte**. A coluna **Status** mostra a situação de cada uma:

- **Aguardando processamento** e **Processando**: o Revodesk está lendo o conteúdo.
- **Pronta para a IA**: o agente já pode consultar.
- **Não foi possível processar**: aparece o motivo e o botão **Tentar novamente**.

Na lista de bases, o status resume tudo: **Sincronizada**, **Aprendendo…**, fontes com erro ou **Sem fontes**.

{% hint style="warning" %}
PDF digitalizado (foto de papel) não tem texto para a IA ler. Use PDFs em que dá para selecionar o texto.
{% endhint %}

### Teste a base

Clique em **Testar uma pergunta**, escreva uma pergunta como um cliente faria e clique em **Buscar**. Você vê os trechos que a IA consultaria para responder.

Se os trechos não têm a ver com a pergunta, falta conteúdo na base ou o texto está pouco claro. Ajuste a fonte e teste de novo.

## 2. Adicione o agente no fluxo

1. Volte ao editor (na barra do projeto, clique em **Fluxos**).
2. Na paleta, em **Agente de IA**, arraste **Agente IA** para o canvas.
3. Ligue o bloco anterior (por exemplo, o **Início**) ao agente.
4. Dê dois cliques no card do agente para abrir o painel **Agente de IA**.

### Instruções

Escreva como o agente deve se comportar: quem ele é, o tom de voz, o que pode e o que não pode fazer. Exemplo:

> Você é a assistente virtual da Loja Exemplo. Responda de forma curta e simpática. Use apenas as informações da base de conhecimento. Se não souber a resposta, diga que vai chamar alguém da equipe.

As instruções aceitam variáveis, como `{{nomeCliente}}`.

### Bases de conhecimento

Clique em **Selecione bases...** e marque as bases que o agente deve consultar. Cada base mostra quantas fontes estão prontas.

<!-- PRINT: painel "Agente de IA" com as Instruções preenchidas e o seletor "Bases de conhecimento" aberto, mostrando uma base marcada -->

### Ferramentas

Em **Ferramentas**, clique em **Adicionar** para que o agente possa agir em outros sistemas durante a conversa, como consultar a agenda ou um pedido. Depois de escolher a ferramenta:

- **Nome**: um nome para você reconhecer a ferramenta.
- **Quando usar**: opcional. Explique em que situação o agente deve usar a ferramenta.
- Escolha a conta conectada e preencha a configuração.

As contas vêm das [Integrações do projeto](integracoes.md).

### Mídia que a IA pode enviar

Por padrão, o agente responde só com texto. Para que ele envie arquivos:

- Marque os formatos permitidos: **Imagem**, **Vídeo**, **Áudio** ou **Documento**.
- Use **Enviar arquivo** para cadastrar um arquivo fixo, como uma tabela de tamanhos. Dê um **Nome** e diga quando enviar.
- Use **Por variável/URL** quando o arquivo vem de uma ferramenta, como a foto de um produto.

## 3. Cadastre as intents

As intents são os momentos em que a conversa deve sair do agente. Cada intent vira uma saída no card.

1. Em **Intents**, clique em **Adicionar**.
2. Em **Nome da intent**, escreva algo curto, como "Falar com atendente".
3. No campo de baixo, descreva quando ela acontece: "O cliente pede para falar com uma pessoa ou demonstra irritação".
4. Feche o painel com **Salvar**.
5. No canvas, ligue a saída da intent ao próximo passo. Para "Falar com atendente", use o bloco **Atendimento humano**.

<!-- PRINT: card do Agente IA no canvas com duas intents, cada uma ligada a um bloco diferente -->

{% hint style="warning" %}
Sem intents, o agente não tem saída: ele nunca passa a conversa adiante. Cadastre pelo menos uma intent para chamar a equipe.
{% endhint %}

## Ajustes avançados

Em **Avançado** ficam o **Modelo** de IA, a **Temperature** (quanto o agente varia nas respostas), o **Max tokens** (tamanho máximo da resposta) e a **Variável de resposta**, onde a última resposta do agente fica guardada. Os valores padrão atendem a maioria dos casos.

## 4. Teste

Clique em **Testar** na barra do editor e converse com o agente. Na aba **Logs**, você vê quais trechos da base ele consultou e quais ferramentas usou.

{% hint style="success" %}
Teste perguntas que seus clientes fazem de verdade. Quando o agente errar, quase sempre a solução é melhorar a base ou as instruções.
{% endhint %}

## Próximos passos

Veja como entregar a conversa para a equipe: [Passando para um atendente humano](atendimento-humano.md).
