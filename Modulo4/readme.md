# Desafio de Modelagem e Transformação de Dados com DAX - Power BI

## 📝 Descrição do Projeto

Este projeto faz parte de um desafio para criar um modelo dimensional no Power BI usando dados financeiros de vendas. A tabela original **Financial Sample** foi transformada em tabelas de dimensão e fato, seguindo o esquema em estrela, otimizando as consultas e permitindo análises detalhadas.

## 📊 Etapas do Desenvolvimento

### 1️⃣ Criação das Tabelas Dimensão e Fato

A partir da tabela principal, foram criadas as seguintes tabelas de dimensão:

- **D_Produtos:** Contendo `ID_produto`, `Produto`, `Média de Unidades Vendidas`, `Médias do valor de vendas`.
- **D_Produtos_Detalhes:** Inclui colunas como `Sale Price`, `Units Sold` e `Manufacturing Price`.
- **D_Descontos:** Armazena informações sobre descontos aplicados, baseadas no `Discount Band`.
- **D_Calendário:** Criada automaticamente com a função DAX `CALENDARAUTO()`.

### 2️⃣ Aplicação de Funções DAX - Tabela Calendário

A tabela de calendário foi gerada a partir da função `CALENDARAUTO()`, abrangendo todas as datas da tabela principal. As colunas adicionais incluem:

- **Ano:**
  ```DAX
  Year = YEAR(D_Calendário[Date])
  Month = FORMAT(D_Calendário[Date], "MMMM")
  Quarter = "Q" & QUARTER(D_Calendário[Date])

  Essas colunas ajudam a segmentar e organizar os dados de forma mais detalhada, permitindo análises temporais eficientes.

🚀 Como Executar o Projeto
Baixar o arquivo PBIX: Abra o arquivo projeto_dash_e-commerce_modulo4.pbix no Power BI.
Conectar aos dados: Verifique se a planilha Financial_Sample_Modulo4.xlsx está conectada corretamente ao Power BI.
Explorar o modelo dimensional: Examine as tabelas e colunas criadas, e veja como os dados foram modelados para otimizar as análises.
