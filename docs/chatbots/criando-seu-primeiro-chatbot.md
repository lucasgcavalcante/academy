# Criando seu primeiro chatbot

## Passo a passo rápido

1. **Abrir o editor / criar novo flow**
   *   Vá pro workspace e crie um novo canvas. Nomeie o flow (ex: `fluxo_suporte`).\
       <br>

       <figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>


2. **Colocar o nó inicial**
   * Arraste pro workspace o primeiro nó (pode ser um `Enviar mensagem` ou um `Start` se tiver).
   * Edite o texto de boas-vindas: `Olá! Eu sou o assistente. Como posso ajudar você hoje?`\
     ![](<../.gitbook/assets/image (6).png>)
3. **Adicionar nós essenciais**
   * Arraste `Enviar botões` logo após a mensagem inicial (ex.: Botões: `Suporte`, `Vendas`, `Outros`).
   * Para cada botão, crie uma **aresta** (edge) que leva ao próximo nó correspondente.
4. **Conectar nós**
   * Clique/arraste do handle de saída do nó até o handle de entrada do nó destino.
   * Sempre **rotule a aresta** com condição legível (ex.: `Botão == Suporte`, `Botão == Vendas`) — isso facilita debug e leitura do flow.
5. **Fazer pergunta (coletar variável)**
   * Arraste `Fazer pergunta` quando precisar de dado (nome, telefone, CPF).
   * Configure:
     * Pergunta: `Qual seu telefone?`
     * Nome da variável: `user.phone`
     * Validação: ex.: regex `^\d{10,11}$` (opcional)
     * Timeout (ex.: 30s) e fallback (ex.: repetir 1x ou transferir para fila)
     * Arestas de saída: `Resposta válida` e `Timeout/Inválida`
6. **Verificar expediente**
   * Use o nó `Verificar expediente` antes de transferir para atendimento humano.
   * Configure fuso/hora de início/término.
   * Duas ramificações típicas: `Dentro do expediente` → continuar / `Fora do expediente` → mensagem de aviso + ação (agendar, fila noturna, sair do bot).
7. **Transferências**
   * `Transferir para uma fila`: configure `queue_id`, enviar metadados (variáveis coletadas como `user.name`, `user.phone`, `última_mensagem`).
   * `Transferir para um usuário`: configure `user_id` ou lógica de roteamento por skill.
   * Garanta que, antes da transferência, você tenha enviado um resumo ao atendente (últimas respostas e tags).
8. **Adicionar etiqueta**
   * Use para marcar a conversa (ex.: `high-priority`, `agendado`, `falso-contato`).
   * Boa prática: etiquetas curtas e padronizadas.
9. **Sair do bot**
   * `Sair do bot` deve encerrar o turno do bot, mantendo a conversa em espera/holding.
   * Configure status a ser enviado pro backend (`on_hold`, `waiting_for_agent`) e mensagem final opcional.
10. **Salvar e testar**
    * Salve o flow.
    * Use modo preview / simulação e teste:
      * Caminho feliz (happy path)
      * Inputs inválidos
      * Timeout
      * Fora do expediente
      * Transferência (ver se metadados chegam no atendimento)
