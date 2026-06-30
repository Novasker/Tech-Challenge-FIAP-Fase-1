# Tech Challenge - Análise e Otimização do Net Promoter Score (NPS)

Este projeto foi desenvolvido como parte do Tech Challenge da pós-graduação em AI Scientist da FIAP. O objetivo principal é identificar quais fatores operacionais realmente influenciam a satisfação do cliente e como a empresa pode agir de forma proativa para melhorar sua experiência.

## Objetivo do Projeto

Este projeto visa realizar uma Análise Exploratória de Dados (EDA) focada em negócio para:
1. Quais fatores parecem mais críticos para a satisfação? 
2. O que mais gera detratores? 
3. Existe algum “ponto de ruptura” na experiência do cliente? 
4. Que tipo de cliente tende a ter NPS mais alto ou mais baixo?

---

## Descrição da Base de Dados

O modelo utiliza a base de dados localizada em `data/desafio_nps_fase_1.csv`, que contém 2.500 registros de clientes e 19 variáveis operacionais e demográficas:

| Variável | Descrição |
| :--- | :--- |
| `customer_id` | Identificador único do cliente. |
| `order_id` | Identificador único do pedido. |
| `customer_age` | Idade do cliente. |
| `customer_region` | Região geográfica do cliente. |
| `customer_tenure_months` | Tempo de relacionamento do cliente com a empresa (em meses). |
| `order_value` | Valor total do pedido. |
| `items_quantity` | Quantidade de itens no pedido. |
| `discount_value` | Valor de desconto aplicado ao pedido. |
| `payment_installments` | Número de parcelas do pagamento. |
| `delivery_time_days` | Tempo total de entrega (em dias). |
| `delivery_delay_days` | Quantidade de dias de atraso na entrega. |
| `freight_value` | Valor do frete. |
| `delivery_attempts` | Número de tentativas de entrega. |
| `customer_service_contacts` | Número de contatos do cliente com o atendimento. |
| `resolution_time_days` | Tempo para resolução de problemas (em dias). |
| `complaints_count` | Número de reclamações registradas pelo cliente. |
| `repeat_purchase_30d` | Indica se houve recompra em até 30 dias após o pedido (0 = não, 1 = sim). |
| `csat_internal_score` | Score interno de satisfação do cliente. |
| `nps_score` | Nota de satisfação do cliente (NPS), variando de 0 a 10, coletada após a experiência de compra. |

---

## Metodologia Utilizada

O projeto foi estruturado seguindo o framework **CRISP-DM**, garantindo o alinhamento entre a estatística e os objetivos de negócio:

1. **Entendimento do Negócio:** Alinhamento do problema com metas financeiras e de retenção.
2. **Entendimento dos Dados:** Análise das variáveis contra o `nps_score`.
3. **Preparação dos Dados:** Segmentação dos clientes nos grupos do NPS (Promotores, Passivos, Detratores)
4. **Modelagem & Análise Exploratória:** Geração de estatísticas descritivas e criação de visualizações de dados.

---

## Como Reproduzir os Resultados

### 1. Pré-requisitos
Certifique-se de ter o Python 3.x instalado. Recomenda-se a utilização de um ambiente virtual ou diretamente pelo Google Colab/Jupyter Notebook.

As bibliotecas necessárias para rodar o projeto são:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `plotly`

Você pode instalá-las via terminal com o comando:
```bash
pip install pandas numpy matplotlib seaborn plotly
