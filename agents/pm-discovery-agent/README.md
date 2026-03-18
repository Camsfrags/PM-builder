# PM Discovery Agent

## O que faz
Estrutura o processo de discovery e desk research combinando três frameworks complementares:
Continuous Discovery Habits (Teresa Torres), JTBD (Jobs To Be Done) e Secondary Research com
Opportunity Mapping. Mapeia os jobs reais dos usuários, constrói uma Opportunity Solution Tree,
identifica gaps de mercado e gera insights acionáveis antes de qualquer linha de código ser escrita.
Funciona para qualquer produto, mercado ou audiência.

## Quando usar
- Antes de iniciar o desenvolvimento de um novo produto ou feature
- Quando você precisa mapear oportunidades usando a Opportunity Solution Tree de Teresa Torres
- Quando precisa entender os jobs reais dos usuários (não o que eles pedem, mas o que tentam realizar)
- Antes de uma rodada de discovery primária (para chegar nas entrevistas com hipóteses bem formadas)
- Quando precisa mapear o landscape competitivo e identificar oportunidades não atendidas

## Inputs esperados
```json
{
  "product_description": "O que você está explorando (produto, feature ou espaço de problema)",
  "target_audience": "Perfil detalhado de quem você quer entender",
  "research_goal": "A pergunta central que você precisa responder",
  "available_resources": {
    "time": "Ex: 1 semana",
    "tools": "Ex: Google, Reddit, G2, SimilarWeb, SEMrush",
    "existing_data": "Ex: 50 tickets de suporte, NPS de 32"
  }
}
```

## Outputs
Markdown estruturado com: Desired Outcome, Opportunity Solution Tree (OST), User Jobs (JTBD),
Pain Points, Market Gaps, Competitive Landscape, Assumption Mapping e Recommended Discovery Cadence.

## Frameworks utilizados
- **Continuous Discovery Habits — Teresa Torres:** Desired outcome, Opportunity Solution Tree,
  assumption mapping, weekly discovery cadence
- **JTBD (Jobs To Be Done):** Functional, emotional e social jobs no formato "When / I want / So I can"
- **Secondary Research + Opportunity Mapping:** Desk research estruturado em fontes públicas
  (reviews, forums, market reports, competitor data)

## Como usar
1. Descreva o produto ou espaço de problema que você está explorando
2. Defina o perfil do usuário-alvo com o máximo de especificidade
3. Formule a pergunta central de pesquisa que você precisa responder
4. Liste os recursos disponíveis (tempo, ferramentas, dados existentes)
5. Execute o agente e use a OST gerada para guiar sua discovery primária semanal

## Exemplo real
**Produto:** App de gestão financeira para freelancers brasileiros com MEI
**Goal:** Entender por que freelancers abandonam ferramentas de controle financeiro após 30 dias
**Resultado:** O agente mapeou o desired outcome ("controlar minhas finanças sem precisar de contador"),
construiu uma OST com 5 oportunidades priorizadas, identificou 5 JTBD jobs e detectou que nenhum
concorrente atende o job "reconciliar receitas com DAS mensal sem conhecimento contábil"
