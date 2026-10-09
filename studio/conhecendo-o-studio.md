# Conhecendo o Studio

Entenda o que é um projeto no Studio e onde fica cada parte dele.

{% hint style="info" %}
Tempo de leitura: 4 min · Para quem: gestores e quem monta automações
{% endhint %}

<!-- VÍDEO: cole aqui o link do YouTube com {% embed url="..." %} -->

## O que é o Studio

O Studio é onde você constrói as experiências conversacionais do Revodesk: os fluxos que conversam com o cliente, os agentes de IA e as integrações com outras ferramentas.

Para abrir, clique em **Studio** no menu lateral.

{% hint style="warning" %}
Se o item **Studio** não aparece no seu menu, seu cargo não tem permissão para gerenciar chatbots. Fale com o administrador da sua conta.
{% endhint %}

## A lista de projetos

Tudo no Studio fica organizado em **projetos**. Um projeto agrupa os fluxos, as bases de conhecimento e as integrações de uma mesma automação. Por exemplo: um projeto "Atendimento da loja" com o fluxo principal, uma base com as perguntas frequentes e a conta do Google Agenda conectada.

<!-- PRINT: tela Studio com a lista de projetos, mostrando o botão "Novo projeto", o campo "Buscar projeto" e as colunas Projeto, Status, Criado em e Atualizado em -->

Na lista você encontra:

- **Projeto**: o nome do projeto e quantos fluxos ele tem. Clique no nome para abrir o editor.
- **Status**: se o projeto está **Ativo** ou **Inativo**.
- **Criado em** e **Atualizado em**: datas de criação e da última alteração.
- **Menu da linha** (os três pontinhos): **Abrir no editor** ou **Excluir**.

Use o campo **Buscar projeto** para encontrar um projeto pelo nome.

{% hint style="warning" %}
Excluir um projeto remove também todos os fluxos dele. Não dá para desfazer.
{% endhint %}

## Dentro do projeto: o editor de fluxo

Ao abrir um projeto, você cai no editor do fluxo de entrada, aquele por onde toda conversa começa. O editor tem três áreas.

<!-- PRINT: editor de fluxo inteiro, com a barra do topo, a paleta de blocos à esquerda e o canvas ao centro com o bloco "Início" -->

### Barra do topo

- **Seta para voltar**: volta para a lista de projetos.
- **Caminho Studio / projeto / fluxo**: clique no nome do fluxo para ver os **Fluxos do projeto**, trocar de fluxo, renomear, excluir ou criar um **Novo fluxo**. O fluxo de entrada aparece com a marca **entrada**.
- **Rascunho** ou **Publicado**: mostra se há alterações que ainda não foram ao ar.
- **Salvando…** e **Salvo**: o editor salva sozinho enquanto você trabalha.
- **Engrenagem (Configurações do projeto)**: onde ficam as variáveis e os secrets do projeto.
- **Testar**: abre um chat de teste ao lado do canvas.
- **Publicar**: coloca as alterações no ar.

### Paleta de blocos (à esquerda)

Lista todos os blocos que você pode usar, separados por categoria. Arraste um bloco para o canvas para usá-lo. Você conhece cada um na aula [Os blocos do fluxo](blocos-do-fluxo.md).

No rodapé da paleta fica **Recursos do projeto**, com atalhos para:

- **Base de conhecimento**
- **Integrações**
- **Variáveis** (abre as configurações do projeto)

### Canvas (ao centro)

É a área onde você monta o fluxo, ligando um bloco ao outro. No canto inferior esquerdo ficam o minimapa e os controles de zoom: **Diminuir zoom**, **Aumentar zoom** e **Ajustar à tela**.

## As páginas do projeto

Quando você abre **Base de conhecimento** ou **Integrações**, o projeto aparece com uma barra lateral própria.

<!-- PRINT: página Base de conhecimento com a barra lateral do projeto aberta, mostrando o seletor de projeto no topo e os grupos Construir e Projeto -->

- **No topo**: o nome do projeto. Clique para trocar de projeto ou em **Ver todos os projetos** para voltar à lista.
- **Construir**: **Fluxos** (volta ao editor), **Base de conhecimento** e **Integrações**.
- **Projeto**: **Variáveis** e **Configurações**, que levam ao editor do projeto.

{% hint style="info" %}
Você vai ver **Agentes** com a marca **em breve**, tanto na barra do projeto quanto na paleta. Ainda não está disponível. Hoje, para usar IA, você coloca o bloco **Agente IA** dentro de um fluxo.
{% endhint %}

## Próximos passos

Agora que você conhece o Studio, monte seu primeiro fluxo: [Montando seu primeiro fluxo](primeiro-fluxo.md).
