# Preparando o público do disparo

Organize quem vai receber a mensagem antes de montar o disparo.

{% hint style="info" %}
Tempo de leitura: 5 min · Para quem: gestores
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## Duas formas de escolher o público

No passo **Público** do assistente de disparo, você escolhe os destinatários de um destes jeitos:

- **Contatos da agenda**: você marca contatos que já estão no Revodesk.
- **Importar planilha CSV**: você envia uma planilha com nomes, telefones e os valores das variáveis.

Escolha a forma que combina com a sua lista. Um disparo usa uma ou outra.

<!-- PRINT: passo Público do assistente de disparo, mostrando o seletor "Contatos da agenda" / "Importar planilha CSV" -->

## Usando os contatos da agenda

### Prepare antes

Os contatos precisam estar cadastrados no Revodesk. Para encontrar o público certo com rapidez, organize-os com etiquetas, como "Clientes VIP" ou "Evento outubro".

- [Cadastrando contatos](../contatos/cadastrando-contatos.md)
- [Organizando com etiquetas](../contatos/etiquetas.md)

### Selecione no assistente

1. Em **Buscar por nome ou telefone…**, digite para filtrar a lista.
2. Em **Etiquetas**, marque uma ou mais etiquetas para mostrar só os contatos que as têm.
3. Marque a caixa ao lado de cada contato que vai receber o disparo.
4. Para marcar de uma vez todos os contatos que aparecem na página, use **Selecionar visíveis**.

A lista mostra 50 contatos por página. Se o filtro trouxer mais, use a paginação abaixo da lista e marque **Selecionar visíveis** em cada página.

À direita, o painel **Selecionados** mostra quem já está na lista e quantos são. Você pode remover um contato por ali ou clicar em **Limpar tudo** para recomeçar.

<!-- PRINT: passo Público com o filtro de Etiquetas aplicado, alguns contatos marcados e o painel "Selecionados" à direita -->

{% hint style="success" %}
A seleção se mantém quando você troca a busca ou a etiqueta. Dá para montar o público em partes: filtre por uma etiqueta, marque, troque o filtro e marque mais.
{% endhint %}

### Preencha as variáveis do template

Se o template escolhido tem variáveis, aparece o quadro **Variáveis do template**. Para cada variável, diga de onde vem o valor:

- **Nome do contato**: usa o nome cadastrado de cada contato.
- **Número do contato**: usa o telefone de cada contato.
- **Valor fixo**: o mesmo texto para todos. Digite o valor no campo ao lado.

O assistente só avança quando todas as variáveis têm uma origem e todos os valores fixos estão preenchidos.

<!-- PRINT: quadro "Variáveis do template" com uma variável ligada a "Nome do contato" e outra a "Valor fixo" com o valor preenchido -->

## Usando uma planilha CSV

Use essa opção quando os contatos não estão no Revodesk ou quando cada pessoa precisa de um valor diferente nas variáveis, como um número de pedido.

### Monte a planilha

- A primeira linha é o cabeçalho, com o nome das colunas.
- Uma coluna **nome** e uma coluna **telefone**, com DDD.
- Se o template tem variáveis, uma coluna para cada uma, com o mesmo nome da variável.
- As colunas são separadas por vírgula.

Exemplo para um template com as variáveis `{{nome}}` e `{{pedido}}`:

```
nome,telefone,pedido
Maria Souza,11999998888,12345
João Lima,21988887777,12346
```

Nesse caso, a coluna `nome` serve ao mesmo tempo como nome do contato e como valor da variável.

{% hint style="warning" %}
O arquivo precisa usar **vírgula** como separador. Algumas versões do Excel em português salvam o CSV com ponto e vírgula; nesse caso o Revodesk não encontra as colunas. Também não use vírgulas dentro dos valores, como em "Souza, Maria".
{% endhint %}

### Envie a planilha

1. Selecione **Importar planilha CSV**.
2. Clique em **Escolher planilha CSV** e escolha o arquivo.
3. Confira o nome do arquivo e o total de contatos válidos que aparecem na tela.

Linhas sem nome, sem telefone ou com alguma variável em branco são ignoradas. Para usar outro arquivo, clique em **Trocar arquivo**.

{% hint style="warning" %}
Escolha o template antes de enviar a planilha. Se você trocar o template depois, a planilha é descartada e precisa ser enviada de novo.
{% endhint %}

## Boas práticas

- Envie apenas para quem espera receber sua mensagem. Contatos que bloqueiam ou denunciam a mensagem podem levar a Meta a pausar o template e afetar a qualidade do seu número.
- Comece com um público pequeno para testar o texto antes de um envio grande.

## Próximos passos

Com o público pronto, monte o disparo: [Criando um disparo passo a passo](criando-disparo.md).
