# 🧾 Projeto Power BI — Análise Comercial (Vendas, Itens, Cobertura e Faturamento)

## 🎯 Propósito do projeto

Dashboard interativo criado no **Power BI** para analisar o desempenho comercial ao longo do tempo, acompanhar cobertura de clientes e simular cenários (What-If). O objetivo é fornecer informações acionáveis para forças de vendas e gestão: identificar produtos/vendedores de destaque, monitorar evolução anual e validar metas.

---

<img width="1260" height="699" alt="image" src="https://github.com/user-attachments/assets/e2363983-82c6-4174-a7b9-2a74ead8b245" />

<img width="1269" height="703" alt="image" src="https://github.com/user-attachments/assets/33d700d0-479b-4bfc-bee4-5e46b6d66437" />

<img width="1260" height="705" alt="image" src="https://github.com/user-attachments/assets/d524ecae-f3c7-40c8-91da-57c63e74830f" />

<img width="1260" height="705" alt="image" src="https://github.com/user-attachments/assets/d4520a80-3df8-489a-a9b7-8e2f0248ffcb" />

<img width="1261" height="713" alt="image" src="https://github.com/user-attachments/assets/8ac75242-8d57-498f-b973-1dae7cfd949c" />

<img width="1264" height="696" alt="image" src="https://github.com/user-attachments/assets/3212b9ed-d9a4-441a-85b0-2dbdf5865da1" />

---

## ⚙️ Tecnologias utilizadas

* **Power BI Desktop** (visualizações, layout e interatividade)
* **Power Query** (ETL: limpeza e transformação)
* **DAX** (medidas e cálculos: faturamento, ticket médio, cobertura, %alcance meta, etc.)
* **Fonte:** arquivos tabulares (CSV / Excel) — representados no modelo de dados

---

## 🧱 Estrutura do modelo de dados (visível nas imagens)

Modelo no formato **Star Schema** com:

* **fVendas (fato)** — colunas principais: cdCliente, cdProduto, cdVendedor, DataEmissao, DataVencimento, qtdItens, valorUnitario, pesoLiquido.
* **dProduto**, **dCliente**, **dVendedor**, **dCalendario** (dimensões).
* **fMetas** (fato/lookup de metas por vendedor e data).
* Tabela auxiliar **Aumento** usada para o cenário *What-If* (campo `Aumento Value`).
* Medidas (lista parcial observada): Faturamento, Meta, % Alcance Meta, Cobertura Cliente, Qtde Vendas, Qtde Itens, Ticket Médio (Venda), Peso (ton).

Essa modelagem facilita filtros por gerente/supervisor/vendedor e análises temporais.

---

## 📊 KPIs principais (conforme imagens)

* **Qtde Vendas:** 158K
* **Qtde Itens:** 18M
* **Cobertura de Clientes:** 1.375 (clientes cobertos)
* **Faturamento total (ex.: painel):** $500,89M
* **Evolução por ano (faturamento):** 2020 = $63M → 2021 = $190M → 2022 = $248M
* **Qtde Vendas ao longo do tempo:** 2020 = 18K → 2021 = 91K → 2022 = 49K
* **Ticket Médio por ano:** 2020 = $3,6K → 2021 = $2,1K → 2022 = $5,1K
* **% Alcance Meta (atual):** 81,80% — **What-If (com aumento de ~5%)** → 85,90%

---

## 🔎 Principais insights (visuais & interpretativos)

* **Crescimento de faturamento (2020→2022):** forte avanço nominal — faturamento cresce ano a ano, apesar de queda na quantidade de vendas em 2022.
* **Ticket médio saltou em 2022:** mesmo com menos vendas, o ticket médio aumenta significativamente em 2022 (sugere foco em itens de maior valor ou mudança de mix).
* **Cobertura está estável/alta:** ~1.3k clientes cobertos; pequeno aumento em 2021 e leve manutenção em 2022.
* **Distribuição de desempenho por vendedor / grupo de produto:** painéis mostram top-performers (vendedores com maior quantidade, grupos sem grupo / carnes / congelados liderando em itens/faturamento).
* **Regiões / estados com maior participação:** painéis Top5 por estado destacam mercados prioritários (ex.: MT, RS, MS, PR, SC).
* **Impacto do What-If:** um pequeno aumento percentual (ex.: +5%) eleva o % de alcance de meta de ~81,8% para ~85,9% — útil para planejar ações comerciais.

---

## 🗂️ Páginas do relatório (conforme imagens)

* **Quantidade de Vendas** — foco em Qtde Vendas por vendedor / grupo / estado.
* **Quantidade de Itens** — análise de volume de itens por vendedor, grupo e estado.
* **Cobertura de Clientes** — número de clientes cobertos por vendedor/grupo/estado.
* **Faturamento** — receita por vendedor, grupo de produto e estado.
* **Evolução** — séries temporais: faturamento, cobertura, quantidade e ticket médio por ano.
* **What If** — simulações com parâmetro de aumento (%), mostrando impacto em % Alcance Meta.

---

## 📈 Boas práticas e pontos técnicos implementados (visíveis)

* Modelagem estrela (melhor performance e simplicidade para DAX).
* Tabela de metas separada (`fMetas`) para comparações e cálculo de %alcance.
* Tabela de cenário (`Aumento`) para parâmetro What-If (slider + input para testar variações).
* Uso consistente de cartões KPI no topo de cada página para navegação e foco.
* Slicers por ano, mês, gerente, supervisor e vendedor — permitem drill-down operacional.

---

## 📬 Contato

📧 **[msevero.vasconcelos@gmail.com](https://www.linkedin.com/in/mario-severo-4575161b1)**
💼 Desenvolvido por **Mário Severo** | *Data & AI Projects*

---
