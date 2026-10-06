# 🏆 Desafio Master: Construindo um Painel Analítico de Logística

**Contexto Corporativo:**
Você acabou de ser contratado como Analista de Dados Pleno para uma gigante do E-commerce. O Gerente de Operações precisa urgentemente de um relatório visual e dinâmico para analisar o desempenho das entregas no último trimestre. A diretoria vai avaliar seu trabalho não apenas pela precisão matemática, mas pela capacidade de tornar os dados **visualmente claros, analíticos e de rápida interpretação**.

Sua missão é construir do zero uma base de dados, processar as métricas e aplicar uma camada de inteligência visual.

---

## 🏗️ Parte 1: Criação da Base de Dados
Crie uma tabela principal contendo **exatamente 100 registros (linhas)**. Você deve inventar ou gerar esses dados de forma que pareçam reais. Sua tabela deve conter as seguintes colunas iniciais:

1. **ID do Pedido** (Ex: PED-001 até PED-100)
2. **Data da Compra** (Datas variadas no último trimestre)
3. **Data Limite Prometida** (Data limite que o cliente deveria receber)
4. **Data de Entrega Real** (Quando o produto efetivamente chegou)
5. **Categoria do Produto** (Ex: Eletrônicos, Vestuário, Casa e Decoração, Esportes)
6. **Valor do Produto (R$)** (Valores variados)
7. **Custo de Frete (R$)** (Valores variados)

---

## ⚙️ Parte 2: O Motor Analítico (Cálculos e Lógica)
Você deverá adicionar colunas extras à sua base para calcular os seguintes indicadores operacionais, aplicando as funções lógicas e matemáticas adequadas:

* **Valor Total do Pedido:** Produto + Frete.
* **Dias de Diferença na Entrega:** O cálculo entre a data que foi entregue e a data prometida.
* **Status da Entrega:** Aqui você deve criar uma regra lógica. O sistema deve classificar automaticamente como "No Prazo", "Atrasado" ou "Entregue Antecipadamente" com base no cálculo dos dias.
* **Taxa de Risco:** Uma análise onde, se o pedido for da categoria "Eletrônicos" E estiver "Atrasado", ele recebe um alerta de "Risco Alto". Caso contrário, "Normal".

---

## 🎨 Parte 3: Inteligência Visual (Formatação Condicional)
O Gerente não tem tempo de ler linha por linha. O seu painel deve "falar" com ele através das cores e formas. Aplique as seguintes regras de formatação:

1. **Termômetro Financeiro:** Na coluna de *Valor Total do Pedido*, utilize um recurso visual interno nas células que mostre o peso financeiro de cada venda comparada às outras, como se fosse um mini-gráfico dentro da célula.
2. **Semaforização:** Na coluna de *Status da Entrega*, implemente indicadores visuais em forma de símbolos que sinalizem positivamente os pedidos no prazo, em atenção os antecipados, e em alerta crítico os atrasados.
3. **Foco Crítico (Linha Inteira):** Toda vez que um pedido estiver com o status de "Risco Alto" (conforme sua regra da Parte 2), **a linha inteira** desse pedido deve se destacar drasticamente do resto da tabela, chamando a atenção imediata do gestor.

---

## 📊 Parte 4: Resumo Gerencial (Dash de Indicadores)
Em um espaço separado (pode ser ao lado da tabela principal ou no topo), crie uma **Tabela de Resumo** por *Categoria do Produto*. Esta área deve conter:

* A soma do faturamento total por categoria.
* A média do custo de frete por categoria.
* Uma formatação que destaque automaticamente qual categoria trouxe o maior faturamento financeiro.

---

## 🧠 Critérios de Avaliação (O que fará você "passar na experiência"):
* **Zero Fórmulas Manuais Básicas:** Tudo deve ser automatizado. Se eu mudar a Data de Entrega Real de um pedido, o Status, a Taxa de Risco e TODAS as cores e ícones da linha devem mudar instantaneamente.
* **Design Limpo e Profissional:** Não faça um "carnaval" de cores. A criatividade aqui significa usar tons e visuais corporativos que guiem os olhos do usuário para o que importa (os problemas e os recordes). Use paletas sóbrias.
* **Completude:** O arquivo final deve ter os 100 registros solicitados e todas as premissas do enunciado cumpridas.

