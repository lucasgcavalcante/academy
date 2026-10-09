# Criando um template

Monte um modelo de mensagem do WhatsApp, veja a prévia e envie para a aprovação da Meta.

{% hint style="info" %}
Tempo de leitura: 7 min · Para quem: gestores
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## Antes de começar

- Você precisa de uma conexão do **WhatsApp Oficial** conectada. Sem ela, a tela de templates mostra o aviso "Você não possui conexões de WhatsApp API Oficial" e o botão **Configurar conexão WABA**. Veja [Conectando seus canais](../administracao/conectando-canais.md).
- Cada template pertence a uma conexão. Se você tem mais de um número, crie o template na conexão certa.

## Onde ficam os templates

Você chega à tela **Templates WhatsApp** por dois caminhos:

- No menu, clique em **Configurações** e depois em **Modelos de mensagens** (grupo Automação).
- Na tela de **Disparos**, clique no botão **Templates**, no canto superior direito.

A lista mostra o **Nome**, a **Categoria**, o **Status**, o **Idioma** e a data em **Criado em** de cada template. No topo você encontra:

- **Buscar templates...** para procurar pelo nome.
- Os filtros **Status** e **Categoria**.
- A seleção da **Conexão WABA**: a lista mostra só os templates da conexão escolhida.
- **Sincronizar**: traz da Meta os templates dessa conexão e atualiza os status.
- O botão de **Atualizar lista** (ícone de seta circular).
- **Criar modelo**.

<!-- PRINT: tela "Templates WhatsApp" com a lista preenchida, destacando a seleção de Conexão WABA, os filtros Status e Categoria e os botões Sincronizar e Criar modelo -->

{% hint style="success" %}
Criou templates direto no painel da Meta? Clique em **Sincronizar** para que eles apareçam no Revodesk.
{% endhint %}

## Passo a passo

### 1. Abra o editor

1. Na tela **Templates WhatsApp**, escolha a conexão em **Conexão WABA**.
2. Clique em **Criar modelo**.

O editor **Novo modelo** abre com o formulário à esquerda e a prévia da mensagem à direita. A prévia muda conforme você preenche.

<!-- PRINT: editor "Novo modelo" inteiro, com o formulário à esquerda e a prévia do WhatsApp à direita -->

### 2. Preencha as informações básicas

1. Escolha a categoria: **Utilitário**, **Marketing** ou **Autenticação**. Se tiver dúvida, releia [O que são templates](o-que-sao-templates.md).
2. Em **Idioma**, escolha o idioma da mensagem. O padrão é Português (Brasil).
3. Em **Tipo de variável**, escolha como as variáveis serão escritas:
   - **Nome**: variáveis com nome, como `{{nome}}` ou `{{pedido}}`.
   - **Número**: variáveis numeradas, como `{{1}}` e `{{2}}`.
4. Em **Nome do template**, dê um nome interno, como `confirmacao_pedido`. Use apenas letras minúsculas, números e underscore. Enquanto você digita, o Revodesk troca espaços por underscore e apaga letras acentuadas e símbolos.
5. Em **Conexão WhatsApp**, confira a conexão.

{% hint style="warning" %}
Categoria, idioma, nome e conexão não podem ser alterados depois de criar o template.
{% endhint %}

### 3. Monte o conteúdo

**Cabeçalho · Opcional**

Escolha uma das opções:

- **Nenhum**: sem mídia. Aqui você pode, se quiser, escrever um texto de cabeçalho de até 60 caracteres.
- **Imagem**: JPG ou PNG, até 5 MB.
- **Vídeo**: MP4, até 16 MB.
- **Documento**: PDF, até 100 MB.

Para mídia, clique no botão de upload que aparece e escolha o arquivo. Cabeçalho com mídia não tem texto. Para trocar o arquivo, remova o atual pelo ícone de lixeira.

**Corpo da mensagem \***

É o texto principal, com até 1.024 caracteres. É obrigatório.

**Rodapé · Opcional**

Uma linha curta, com até 60 caracteres.

**Botões · Opcional**

Clique em **Adicionar botão** (até 3). Para cada botão, escolha o **Tipo do botão** e escreva o **Texto do botão** (até 25 caracteres):

- **Resposta Rápida**: o contato toca e a resposta volta para a conversa.
- **URL (Link)**: abre um site. Preencha o campo **URL**.
- **Telefone**: liga para um número. Preencha **Número de telefone** no formato internacional, como `+5511999999999`.

<!-- PRINT: seção Botões com dois botões preenchidos, um do tipo Resposta Rápida e outro do tipo URL (Link) -->

### 4. Adicione variáveis (se precisar)

Variáveis deixam a mensagem personalizada para cada contato.

1. No **Corpo da mensagem** (ou no texto do cabeçalho), clique em **Adicionar variável**. O editor insere `{{}}` no fim do texto.
2. Escreva o nome da variável entre as chaves, de acordo com o **Tipo de variável** escolhido. Exemplo com o tipo Nome: `Olá {{nome}}, seu pedido {{pedido}} saiu para entrega.`
3. Logo abaixo aparece **Amostra de variáveis**. Preencha um exemplo para cada uma, como "Maria" e "12345".

Os exemplos aparecem na prévia e vão para a Meta junto com o template. Eles ajudam o revisor a entender a mensagem.

{% hint style="warning" %}
No cabeçalho, só a primeira variável é considerada.
{% endhint %}

<!-- PRINT: corpo da mensagem com duas variáveis e o quadro "Amostra de variáveis" preenchido logo abaixo -->

### 5. Envie para aprovação

1. Confira a prévia à direita.
2. Clique em **Criar template**.

Se tudo estiver certo, aparece a mensagem "Template criado com sucesso! Aguarde a aprovação da Meta." e você volta para a lista. O template entra com o status **Pendente**.

Se faltar algo, o Revodesk avisa. Os avisos mais comuns são nome com menos de 3 caracteres, conexão não selecionada e corpo da mensagem vazio.

## Editando e excluindo

Na lista, clique no menu de ações (⋯) no fim da linha do template:

- **Editar template**: abre o editor. Você pode mudar o conteúdo e o tipo de variável. Ao salvar com **Atualizar template**, as alterações são enviadas de novo para a Meta.
- **Excluir template**: pede confirmação. Esta ação não pode ser desfeita.

{% hint style="warning" %}
Editar um template **Aprovado** faz com que ele volte para **Pendente** e passe por uma nova revisão da Meta. Enquanto isso, ele não aparece na escolha de template de novos disparos.
{% endhint %}

## Dicas para uma boa aprovação

- Escreva com clareza quem está falando e por quê.
- Prefira a categoria que descreve de verdade o conteúdo.
- Preencha exemplos realistas nas variáveis.
- Evite começar ou terminar o texto com uma variável.
- Em botões de link, use endereços do seu próprio site.

A decisão final é sempre da Meta.

## Próximos passos

Veja o que cada status significa e o que fazer em cada caso: [Aprovação da Meta e status do template](aprovacao-e-status.md).
