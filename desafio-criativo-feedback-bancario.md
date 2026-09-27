# Desafio Criativo: Extraindo Insights do Feedback de Clientes Bancários

> Desafio da trilha DIO — construção de um prompt de IA em etapas (intenção, contexto/restrições e prompt final), com exemplo de aplicação.

## 🧱 Passo 1 — Intenção

Quero que a IA analise comentários de clientes sobre atendimento digital de um banco (aplicativo, Pix, cartão de crédito e chat de suporte) para identificar reclamações frequentes, elogios e oportunidades de melhoria.

O resultado será usado pela equipe de Experiência do Cliente (CX) e pelo time de Produtos Digitais para apoiar a priorização de melhorias no aplicativo e nos canais de atendimento.

A entrega deve conter um resumo executivo, uma tabela com os principais temas, exemplos de comentários e recomendações práticas.

O resultado será considerado bom se for claro, organizado, baseado exclusivamente nos comentários fornecidos e útil para priorizar ações.

## 🧱 Passo 2 — Contexto e Restrições

**Contexto:** Estou trabalhando com feedbacks de clientes bancários relacionados ao aplicativo, Pix, cartão de crédito e atendimento por chat.

**Dados disponíveis:** A base contém data do comentário, canal de atendimento (app, chat, agência, telefone), produto citado (conta corrente, cartão de crédito, Pix, empréstimo, investimentos), texto do feedback e nota de satisfação de 1 a 5.

**Critérios de análise:** A IA deve classificar os feedbacks por tema, sentimento, urgência e produto citado.

**Cuidados e restrições:**
- Use apenas os dados fornecidos.
- Não invente números, causas ou conclusões.
- Não exponha dados pessoais ou sensíveis (nomes, CPF, números de conta, etc.).
- Se houver informação insuficiente, indique a limitação.
- Use linguagem simples, direta e voltada para tomada de decisão.

## 🧱 Passo 3 — Prompt Final

```
Atue como analista de dados e experiência do cliente em uma instituição financeira.

Sua tarefa é analisar feedbacks de clientes bancários sobre aplicativo, Pix, cartão de
crédito e atendimento por chat para identificar temas recorrentes, sentimento dos
clientes, urgência dos problemas e oportunidades de melhoria.

Contexto: A análise será usada pela equipe de Experiência do Cliente (CX) e pelo time
de Produtos Digitais para priorizar melhorias no aplicativo, reduzir atritos no
atendimento e direcionar ações corretivas no próximo ciclo.

Dados disponíveis: Uma base de feedbacks contendo data do comentário, canal de
atendimento (app, chat, agência, telefone), produto citado (conta corrente, cartão de
crédito, Pix, empréstimo, investimentos), texto do feedback e nota de satisfação de 1 a 5.

Instruções de análise:
- Classifique cada feedback por tema (ex.: usabilidade do app, lentidão no atendimento,
  cobranças indevidas, elogios ao suporte), sentimento (positivo, neutro, negativo) e
  urgência (baixa, média, alta).
- Identifique os principais padrões, problemas recorrentes, elogios e oportunidades.
- Aponte evidências extraídas diretamente dos dados fornecidos, citando trechos curtos
  dos comentários como exemplo.
- Sugira ações práticas e priorizadas para as equipes de Experiência do Cliente e
  Produtos Digitais.

Formato da resposta:
- Um resumo executivo de até 5 linhas.
- Uma tabela com as colunas: Tema | Sentimento | Urgência | Evidência | Ação sugerida.
- Uma lista final com as 3 prioridades mais importantes a serem tratadas.

Restrições:
- Use apenas os dados fornecidos; não invente números, causas ou conclusões.
- Não exponha dados pessoais ou sensíveis dos clientes.
- Se houver informação insuficiente para alguma classificação, indique claramente essa
  limitação.
- Use linguagem simples, direta e voltada para tomada de decisão executiva.
```

## 🧪 Exemplo de Aplicação

> Base de feedbacks fictícia, criada apenas para demonstrar o funcionamento do prompt.

### Dados de entrada

| Data | Canal | Produto | Feedback | Nota |
|---|---|---|---|---|
| 02/09/2026 | App | Cartão de crédito | "Fatura veio com cobrança que não reconheço, ninguém me explica no chat" | 2 |
| 05/09/2026 | Chat | Pix | "Fiz um Pix errado e o suporte demorou 3 dias pra resolver" | 1 |
| 08/09/2026 | App | Conta corrente | "App trava toda vez que tento ver o extrato" | 2 |
| 10/09/2026 | Telefone | Cartão de crédito | "Atendente muito educado, resolveu rápido meu bloqueio de cartão" | 5 |
| 12/09/2026 | App | Pix | "Adorei a nova tela do Pix, ficou bem mais simples" | 5 |
| 15/09/2026 | Chat | Empréstimo | "Simulação de empréstimo não bate com o valor final, achei confuso" | 2 |
| 18/09/2026 | Agência | Conta corrente | "Fui mal atendido, fiquei 40 minutos na fila sem senha eletrônica funcionando" | 1 |
| 20/09/2026 | App | Investimentos | "Interface de investimentos é ótima, fácil de entender" | 4 |
| 22/09/2026 | Chat | Cartão de crédito | "Chat caiu no meio do atendimento e tive que recomeçar do zero" | 2 |
| 25/09/2026 | App | Pix | "Notificação de Pix recebido demora muito pra aparecer" | 3 |

### Resultado gerado pela IA

**Resumo executivo:** A maior parte das reclamações concentra-se em falhas de atendimento (chat instável, filas longas) e cobranças/valores não claros (fatura, simulação de empréstimo). O app recebe elogios de usabilidade em Pix e investimentos, mas apresenta travamentos pontuais. Os problemas de maior urgência envolvem cobrança indevida e falha no suporte via chat, com risco direto de evasão de clientes.

| Tema | Sentimento | Urgência | Evidência | Ação sugerida |
|---|---|---|---|---|
| Cobrança não reconhecida | Negativo | Alta | "cobrança que não reconheço, ninguém me explica" | Criar fluxo de contestação de fatura com resposta em até 24h |
| Falha no suporte via chat | Negativo | Alta | "chat caiu no meio do atendimento" / demora de 3 dias no Pix | Revisar estabilidade do chat e SLA de resposta |
| Instabilidade do app | Negativo | Média | "app trava toda vez que tento ver o extrato" | Priorizar correção de bugs na tela de extrato |
| Atendimento presencial lento | Negativo | Média | "fiquei 40 minutos na fila sem senha eletrônica" | Verificar funcionamento do sistema de senhas nas agências |
| Clareza em simulações | Negativo | Média | "simulação não bate com o valor final" | Revisar transparência dos cálculos de empréstimo |
| Usabilidade do Pix/Investimentos | Positivo | Baixa | "adorei a nova tela do Pix" / "interface de investimentos é ótima" | Manter padrão de design nessas telas como referência |
| Atendimento telefônico | Positivo | Baixa | "atendente muito educado, resolveu rápido" | Usar como boas práticas em treinamento de equipe |
