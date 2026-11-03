# Porsche Sales Intelligence Dashboard
Dashboard interativa de análise de 100 registros de vendas Porsche, construída em HTML.

### 🔗 Dashboard publicada


### Perguntas de negócio
1. Quais modelos geram maior receita? — barras horizontais com os oito modelos de maior receita no recorte. Ajuda a identificar quais modelos concentram o valor vendido.
2. Como os clientes pagam? — quantidade de registros por método de pagamento. Ajuda a compreender a distribuição dos meios de pagamento.
3. Qual é a situação das entregas? — quantidade de registros por status sanitizado. Ajuda a visualizar o andamento operacional, sem agrupar estados diferentes arbitrariamente.

### Indicadores e filtros
Os indicadores no topo são recalculados conforme os filtros: quantidade de registros, receita registrada, ticket médio e quantidade/percentual com status Delivered.

Filtros combináveis: modelo, estado, ano do veículo, método de pagamento e status de entrega. O campo de ano refere-se ao ano do veículo, não ao ano da venda.

### Tratamento da base
A planilha original contém campos crus e suas versões sanitizadas. Para a dashboard foram mantidos somente:
- sale_id
- SaleDateSanitized → sale_date
- PorscheModelSanitized → model
- ModelYearSanitized → model_year
- SalesPriceSanitized → sale_price_usd
- VehicleMileageSanitized → mileage_miles
- PayMethodSanitized → payment_method
- CitySanitized → city
- StateSanitized → state
- DeliveryStatusSanitized → delivery_status
  
Os valores de preço, ano e quilometragem foram mantidos como numéricos. Datas sanitizadas marcadas como INVALID foram preservadas como marcador; Nomes de clientes e vendedores e todos os campos crus foram excluídos.
Observação de interpretação

### Prompt utilizado
Crie uma dashboard de vendas em um único arquivo HTML, usando exclusivamente os campos sanitizados da planilha Porsche. Não inclua nome de cliente e vendedor. A dashboard deve ser responsiva e ter filtros combináveis por modelo, estado, ano do veículo, método de pagamento e status de entrega. Os indicadores do topo devem recalcular conforme os filtros: quantidade de registros, receita registrada, ticket médio e quantidade/percentual de entregues. Responda a três perguntas: (1) quais modelos geram maior receita? Use barras horizontais e destaque o top 8; (2) como os clientes pagam? Mostre quantidade por método de pagamento; (3) qual é a situação das entregas? Mostre quantidade por status sanitizado. Use identidade visual inspirada em interfaces automotivas premium: fundo grafite/preto, vermelho como destaque, tipografia limpa, cartões discretos e boa responsividade. Inclua botão para limpar filtros e estados vazios quando nenhum registro corresponder.

### Tecnologias e ferramenta
- A estrutura do projeto foi preparada com apoio de IA e revisão dos cálculos/escopo dos dados.
- Chatgpt sem agentes
- Ferramenta CANVAS descontinuada
