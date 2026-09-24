**🧱 Passo 1: Defina a automação desejada**

**Quero criar uma automação no N8N para** gestão automatizada de pedidos de delivery via WhatsApp com validação de pagamento.

**Público ou responsável:** Atendimento ao cliente e equipe da cozinha.

**Resultado esperado:** Capturar o pedido feito pelo cliente, gerar uma cobrança via PIX automaticamente, aguardar a confirmação do pagamento e, assim que pago, registrar o pedido em uma planilha e notificar a cozinha para iniciar o preparo.

**🧱 Passo 2: Adicione contexto e regras**

**Ferramentas envolvidas:** WhatsApp (via Evolution API ou Z-API), Mercado Pago (para PIX), Google Sheets (para histórico de vendas) e Trello (para o painel de produção da cozinha).

**Fluxo desejado:**

1. Receber a mensagem do cliente com os detalhes do pedido (caldos, salgados, etc.).

2. Gerar a cobrança PIX via Mercado Pago e enviar o código copia e cola para o WhatsApp do cliente.

3. Aguardar o webhook de confirmação de pagamento do Mercado Pago.

4. Após o pagamento, salvar os dados do cliente e valor no Google Sheets.

5. Criar um card no Trello para a cozinha com os itens a serem preparados.

**Regras importantes:**

* Se o pagamento não for confirmado em até 15 minutos, o fluxo deve enviar uma mensagem cancelando o pedido automaticamente.

* Ignorar mensagens recebidas fora do horário de funcionamento (após as 23h).

**🧱 Passo 3: Monte o prompt final**

Aqui está a união de todos os elementos, formando um prompt de alta precisão que você pode usar em IAs (como ChatGPT, Claude, Gemini ou DeepSeek) para gerar a estrutura técnica da automação.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Atue como um especialista e arquiteto de fluxos no N8N.

Crie uma automação para gestão automatizada de pedidos de delivery via WhatsApp com validação de pagamento.

Público:

Atendimento ao cliente e equipe da cozinha.

Ferramentas envolvidas:

WhatsApp (Evolution API/Z-API), Mercado Pago, Google Sheets e Trello.

Fluxo:

1\. Receber o pedido do cliente via WhatsApp.

2\. Gerar cobrança PIX e enviar o código copia e cola para o cliente.

3\. Aguardar o webhook de confirmação de pagamento do Mercado Pago.

4\. Salvar os dados financeiros e do cliente no Google Sheets.

5\. Criar um card no Trello informando os itens para a cozinha preparar.

Regras:

\- Implementar uma lógica (Wait/Delay \+ IF): se o pagamento não for confirmado em 15 minutos, cancelar o pedido e avisar o cliente no WhatsApp.

\- Validar o horário: ignorar mensagens e disparar aviso de "Estamos fechados" se o gatilho ocorrer fora do horário de funcionamento.

Com base nisso, explique o passo a passo: 

Quais nós (nodes) exatos do N8N devem ser utilizados (ex: Webhook, HTTP Request, Switch, Wait)? Qual é a lógica de funcionamento e roteamento (ex: como cruzar os dados do webhook de pagamento com o pedido original)?