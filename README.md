👔 Análise de Dados de RH – DAX Avançado

Este repositório apresenta um conjunto de análises em Business Intelligence aplicadas ao setor de Recursos Humanos, desenvolvidas com o Power BI e com ênfase no uso de expressões DAX de nível não trivial.
O objetivo é transformar dados de funcionários em informações claras, explorando cálculos avançados e boas práticas de visualização para apoiar a tomada de decisão.

---

📁 Estrutura das Análises

O projeto foi segmentado em diferentes blocos de perguntas de negócio, cada uma resolvida com expressões DAX específicas:

Contagem de Funcionários – Uso de DISTINCTCOUNT para garantir a contagem correta de IDs únicos.

Resumo Funcionários + Experiência – Medida que concatena número de funcionários e média de anos de experiência em um único card.

Distribuição por Gênero – Total de homens, total de mulheres e respectivos percentuais sobre o quadro geral.

Variáveis e Expressões Avançadas – Criação de medidas com VAR, CALCULATE, DIVIDE e FORMAT para maior legibilidade e desempenho.

Somatórios Específicos por Cargo – Quantificação de funções específicas, como Cientista de Dados.

Promoções – Regras de negócio modeladas via colunas condicionais no Power Query para determinar funcionários aptos à promoção.

Disponibilidade para Hora Extra – Visual em pizza após padronização dos valores (“Sim”/“Não”).

Índice de Envolvimento no Trabalho – Engenharia de atributos para transformar índices numéricos (1–4) em categorias qualitativas (“Ruim”, “Médio”, “Bom”, “Excelente”).

---

🎯 Diretrizes de Visualização

Cards conjugados: Totais e percentuais (masculino/feminino) exibidos em conjunto, evitando redundância.

Engenharia de atributos: Criação de colunas condicionais no Power Query para melhorar a interpretação dos dados.

Uso de Slicers: Segmentação de dados por idade para análises dinâmicas.

Formatação cuidadosa:

Percentuais exibidos como porcentagens (não como decimais).

Substituições de valores categóricos feitas via Power Query.

Caixas e formas usadas apenas para destacar visuais, sem comprometer a interatividade.

---

🧠 Considerações Analíticas
---
🔍 Contagem e Experiência

DISTINCTCOUNT aplicado sobre Id_Funcionario garante contagem correta de indivíduos únicos.

Medida Resumo Funcionários e Experiência combina contagem e média de experiência em um único card, com UNICHAR(10) para quebra de linha.

📈 Distribuição de Gênero

Cálculo de homens e mulheres com CALCULATE filtrando a coluna Genero.

Uso de variáveis (VAR) para clareza, reaproveitamento e eficiência.

Percentuais calculados com DIVIDE para evitar erro de divisão por zero.

---

🗂️ Promoções

Criação de coluna condicional StatusPromo no Power Query para determinar elegibilidade (≥ 5 anos = promover).

Medidas derivadas: TotalFuncPromover, TotalNaoPromover, %Promover.

---

🏷️ Outras Métricas Relevantes

Salário médio: AVERAGE(DatasetRH[Salario_Mensal]).

Engajamento: Conversão de escala numérica para categorias literais.

Disponibilidade para hora extra: Padronização “S/N” → “Sim/Não”.

---

🧩 Boas Práticas Adotadas

Organização das medidas em tabelas dedicadas (Medidas) para evitar poluição do dataset.

Padronização de colunas com Text.Trim, Text.Clean, Text.Upper.

Verificação de valores distintos com VALUES(DatasetRH[StatusPromo]) para evitar erros de escrita.

Sempre validar se o visual atende à audiência: clareza > estética.

---
🛠️ Ferramentas Utilizadas

Power BI

Power Query (M Language)

DAX (expressões avançadas)

Git e GitHub

---

📂 Estrutura do Projeto
📁 Projeto_RH
 ┣ 📄 ProjetoRH.pbix
 ┣ 📄 README.md

---

🚀 Como Visualizar

Baixe o arquivo .pbix deste repositório

Abra-o no Power BI Desktop

Navegue entre as páginas e explore as medidas criadas em DAX

---

🤝 Conecte-se comigo no [LinkedIn](https://www.linkedin.com/in/rafael-paiva-martins/) 
 para acompanhar mais projetos, discutir expressões DAX ou colaborar em soluções de análise de dados.
---

 👔 HR Data Analysis – Advanced DAX Applications

This repository presents a set of Business Intelligence analyses applied to Human Resources, developed with Power BI and focusing on the use of non-trivial DAX expressions.
The goal is to transform HR data into actionable insights by leveraging advanced calculations and visualization best practices to support decision-making.

---

📁 Analysis Structure

The project is segmented into several business questions, each solved with specific DAX measures:

Employee Count – Using DISTINCTCOUNT to correctly count unique employee IDs.

Employees + Experience Summary – A combined card displaying employee count and average years of experience in a single measure.

Gender Distribution – Total of male and female employees, plus their percentage of the overall workforce.

Variables and Advanced Expressions – Creating measures with VAR, CALCULATE, DIVIDE, and FORMAT for readability and performance.

Role-Specific Totals – Summaries for specific job titles, e.g., Data Scientist.

Promotion Eligibility – Business rules modeled via conditional columns in Power Query to identify employees eligible for promotion.

Overtime Availability – Pie chart after standardizing values (“Yes”/“No”).

Work Engagement Index – Feature engineering to map numeric indexes (1–4) into qualitative categories (“Poor”, “Average”, “Good”, “Excellent”).

---

🎯 Visualization Guidelines

Conjugated cards: Totals and percentages (male/female) shown together, avoiding redundancy.

Feature engineering: Conditional columns created in Power Query to improve interpretation.

Slicers: Age slicers allow dynamic filtering across visuals.

Careful formatting:

Percentages displayed properly instead of decimals.

Standardization of categorical values via Power Query.

Shapes and boxes used for layout clarity, without compromising interactivity.

---

🧠 Analytical Highlights
🔍 Counting and Experience

DISTINCTCOUNT on Id_Funcionario ensures unique employee counts.

Measure Employees and Experience Summary concatenates employee count and average years of experience in one card, using UNICHAR(10) for line breaks.

📈 Gender Distribution

Male/female totals calculated with CALCULATE filtering the Gender column.

Variables (VAR) improve readability and efficiency.

Percentages calculated with DIVIDE to avoid division by zero errors.

---

🗂️ Promotion Rules

Conditional column StatusPromo created in Power Query to define eligibility (≥ 5 years = eligible).

Derived measures: TotalFuncPromover, TotalNaoPromover, %Promover.

---

🏷️ Other Key Metrics

Average Salary: AVERAGE(DatasetRH[Salario_Mensal]).

Engagement: Numeric index mapped into categories.

Overtime Availability: Standardization of “S/N” → “Yes/No”.

---

🧩 Best Practices

Dedicated Measures tables to keep dataset organized.

Column standardization with Text.Trim, Text.Clean, Text.Upper.

Validation with VALUES(DatasetRH[StatusPromo]) to detect literal mismatches.

Always validate whether the visual is audience-friendly: clarity > aesthetics.

---

🛠️ Tools Used

Power BI

Power Query (M Language)

DAX (advanced expressions)

Git & GitHub

---

📂 Project Structure
📁 HR_Project
 ┣ 📄 HR_Project.pbix
 ┣ 📄 README.md

---

🚀 How to View

Download the .pbix file from this repository

Open it in Power BI Desktop

Navigate through the pages and explore the created DAX measures

---

🤝 Connect

Connect with me on [LinkedIn](https://www.linkedin.com/in/rafael-paiva-martins/) to follow more projects, discuss DAX expressions, or collaborate on data analysis solutions.
