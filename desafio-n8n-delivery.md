Atue como um especialista e arquiteto de fluxos no N8N.
Crie uma automação para gestão automatizada de pedidos de delivery via WhatsApp com validação de pagamento.

Público:
Atendimento ao cliente e equipe da cozinha.

Ferramentas envolvidas:
WhatsApp (Evolution API/Z-API), Mercado Pago, Google Sheets e Trello.

Fluxo:
1. Receber o pedido do cliente via WhatsApp.
2. Gerar cobrança PIX e enviar o código copia e cola para o cliente.
3. Aguardar o webhook de confirmação de pagamento do Mercado Pago.
4. Salvar os dados financeiros e do cliente no Google Sheets.
5. Criar um card no Trello informando os itens para a cozinha preparar.

Regras:
- Implementar uma lógica (Wait/Delay + IF): se o pagamento não for confirmado em 15 minutos, cancelar o pedido e avisar o cliente no WhatsApp.
- Validar o horário: ignorar mensagens e disparar aviso de "Estamos fechados" se o gatilho ocorrer fora do horário de funcionamento.

Com base nisso, explique o passo a passo: 
Quais nós (nodes) exatos do N8N devem ser utilizados (ex: Webhook, HTTP Request, Switch, Wait)? Qual é a lógica de funcionamento e roteamento (ex: como cruzar os dados do webhook de pagamento com o pedido original)?
