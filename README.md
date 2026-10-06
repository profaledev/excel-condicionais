# Dominando a Formatação Condicional no Excel: Do Básico às Fórmulas Lógicas

Olá, turma! Bem-vindos à nossa aula de Excel de hoje.

Se vocês já olharam para uma planilha gigantesca, cheia de números, e se sentiram perdidos sem saber o que é bom, o que é ruim, ou o que precisa de atenção urgente, a aula de hoje vai mudar a vida de vocês. Hoje vamos aprender a fazer o Excel trabalhar para nós usando a **Formatação Condicional**.

## 1. O que é essa tal de Formatação Condicional?

Imaginem que vocês têm uma lista com 500 notas de alunos ou 500 vendas de produtos. Vocês não vão querer pintar de vermelho, uma por uma, as notas vermelhas ou as vendas ruins, certo?

A Formatação Condicional é a mágica que faz o Excel pintar as células **sozinho**, baseado nas regras que **nós** criarmos. Mudou o número? A cor muda junto, automaticamente.

> **Onde isso é usado no Mercado de Trabalho?**
> Absolutamente em TUDO! Empresas não têm tempo de ler linha por linha. Um analista financeiro usa para ver contas vencidas brilhando em vermelho. O pessoal de RH usa para ver quem bateu a meta. Logística usa para ver qual estoque está acabando. Quem sabe fazer isso bem, cria painéis (dashboards) que os chefes adoram bater o olho e entender na hora.

## 2. Exemplos Práticos: Vamos colocar a mão na massa!

Turma, vamos ver cinco formas de usar, da mais simples até a de nível "analista sênior". Abram o Excel aí e vamos juntos!

### Exemplo 1: O Básico (Regras de Realce)

Vamos começar com o clássico: destacar quem está reprovado ou quem vendeu pouco. Nossa regra será: **Nota menor que 6, pinta de vermelho.**

1. Selecionem a coluna das notas.

2. Lá em cima, na guia **Página Inicial**, cliquem em **Formatação Condicional**.

3. Vão em **Regras de Realce das Células** > **É Menor do que...**

4. Digitem `6` e escolham "Preenchimento Vermelho Claro". Pronto!

**Vejam como a tabela se transforma:**

| Aluno | Nota (Sem Formatação) | Como fica no Excel (Com Formatação) | 
| ----- | ----- | ----- | 
| João | 8 | 8 | 
| Maria | 4 | 🔴 **4** *(Fundo vermelho)* | 
| Pedro | 7 | 7 | 
| Ana | 5 | 🔴 **5** *(Fundo vermelho)* | 

*Se a Maria tirar um 7 depois da recuperação, a cor vermelha some sozinha!*

### Exemplo 2: Impacto Visual (Barras de Dados e Ícones)

E se a gente quiser transformar números em gráficos dentro da própria célula? Fica muito profissional e é ótimo para relatórios de vendas.

1. Selecionem a coluna de "Faturamento".

2. **Formatação Condicional** > **Barras de Dados**. Escolham uma cor.

3. Testem também os **Conjuntos de Ícones** (aquelas setinhas coloridas para cima, para o lado e para baixo).

| Vendedor | Faturamento | Barras de Dados (Visual) | Status (Ícones) | 
| ----- | ----- | ----- | ----- | 
| Carlos | R\$ 50.000 | ██████████ *(Barra cheia)* | 🟢 ↑ | 
| Julia | R\$ 30.000 | ██████ *(Barra média)* | 🟡 → | 
| Marcos | R\$ 10.000 | ██ *(Barra pequena)* | 🔴 ↓ | 

### Exemplo 3: A Função "E" (Todas as regras precisam bater)

Agora vamos subir de nível. E se eu quiser pintar a **linha inteira**, mas só se DUAS coisas acontecerem ao mesmo tempo?
Quero destacar de verde o projeto que custa **menos de R\$ 60.000** **E** está **"Concluído"**.

1. Selecionem a tabela toda (sem o cabeçalho!).

2. **Formatação Condicional** > **Nova Regra** > **"Usar uma fórmula..."**.

3. Digitem a nossa regra lógica: `=E($B2<60000; $C2="Concluído")`

4. Cliquem em **Formatar** e escolham o fundo verde.

|  | 
| ----- | 

### Exemplo 4: A Função "OU" (Basta uma regra ser verdade)

E quando qualquer um dos problemas já é motivo de alerta? Pensem na gestão de um estoque. Eu quero que a linha fique amarela se o produto estiver com **Estoque Zero** **OU** se estiver **"Vencido"**. Basta um para dar problema.

1. Selecionem a tabela toda.

2. Nova regra com fórmula: `=OU($B2=0; $C2="Vencido")`

3. Formatem com preenchimento amarelo.

| Produto | Estoque (Col B) | Validade (Col C) | Resultado Visual | 
| ----- | ----- | ----- | ----- | 
| Feijão | 50 | No Prazo | *(Linha Branca)* | 
| **Arroz** | **0** | **No Prazo** | 🟡   $$ LINHA PINTADA DE AMARELO - Estoque zerou $$ | 
| **Leite** | **20** | **Vencido** | 🟡   $$ LINHA PINTADA DE AMARELO - Venceu $$ | 

### Exemplo 5: O Terror do Escritório (Datas e Prazos)

Turma, anotem isso porque chefe adora! Como eu faço para o Excel pintar de vermelho automaticamente uma conta que já venceu, comparando com o dia de **hoje**?
Usamos a função `HOJE()`, que atualiza sozinha todo dia que você abre a planilha!

1. Selecionem a coluna de "Vencimento".

2. Nova regra com fórmula: `=$B2<HOJE()`

3. Preenchimento vermelho e texto em negrito.

| Fatura | Vencimento (Col B) | Resultado Visual (Imaginando que hoje seja 15/10) | 
| ----- | ----- | ----- | 
| Luz | 20/10/2026 | *(Linha Branca - Vai vencer ainda)* | 
| **Água** | **10/10/2026** | 🔴 **10/10/2026** *(Ficou vermelho porque já passou de hoje!)* | 

*(Imaginem o poder disso numa planilha de cobrança!)*

## 3. Desafio Prático: Agora é com vocês!

Chegou a hora de provar que entenderam. Pessoal, construam rapidinho essa tabela aí no Excel de vocês:

| Vendedor | Vendas (R\$) | Satisfação (1 a 10) | Faltas | 
| ----- | ----- | ----- | ----- | 
| Ana Souza | 120.000 | 9 | 1 | 
| Carlos Lima | 85.000 | 7 | 4 | 
| Beatriz Alves | 150.000 | 6 | 0 | 
| João Pedro | 70.000 | 5 | 5 | 
| Fernanda Costa | 110.000 | 8 | 2 | 

**A Missão:**
Vocês são os gerentes dessa equipe e precisam configurar a planilha para dar duas respostas visuais automáticas:

1. **O Bônus Trimestral (Verde):** Usem uma regra com fórmula para pintar a **linha inteira de verde** dos vendedores que venderam 100.000 ou mais **E** tiveram nota de satisfação 8 ou mais. *(Dica: Usem a função E).*

2. **O Alerta de Risco (Amarelo):** Pintem a célula do **nome** do vendedor de amarelo se a satisfação for menor que 6 **OU** ele tiver mais de 3 faltas. *(Dica: Usem a função OU).*

Vão tentando que eu vou passar olhando as mesas de vocês!

## 4. Dicas Finais (Os erros clássicos!)

Turma, antes de liberar vocês, prestem atenção nesses erros comuns que todo mundo comete no início:

* **Esquecer o cifrão (`$`):** Se for pintar a linha toda com fórmula, lembre-se de travar a coluna (ex: `$A2`). Se esquecer, o Excel vai pintar as células como num tabuleiro de xadrez, tudo torto.

* **Texto sem aspas:** Dentro da fórmula da formatação, se for procurar uma palavra (como "Concluído", "Vencido"), coloque entre aspas duplas (`"Vencido"`), senão o Excel dá erro.

* **A Função HOJE():** Não coloquem nada dentro dos parênteses da função HOJE. É só `HOJE()` mesmo. Ela puxa o relógio do seu computador.

* **Ordem das regras:** Se uma célula ficar verde e vermelha ao mesmo tempo por causa de duas regras diferentes, qual cor vence? O Excel lê de cima para baixo. Dá para organizar a prioridade lá em *Formatação Condicional > Gerenciar Regras*.

Bom trabalho a todos, salvem as planilhas e até a próxima aula!