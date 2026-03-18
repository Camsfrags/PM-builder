# PM Roadmap Agent

## O que faz
Estrutura e prioriza roadmaps de produto combinando quatro frameworks complementares: Now/Next/Later
(roadmap agnóstico sem datas), Opportunity Roadmap (Teresa Torres — conectado à OST), JTBD Roadmap
(priorizado por jobs do usuário) e OKR-driven Roadmap (cada item conectado a um objetivo estratégico).
Gera um roadmap com justificativa de priorização para cada item e narrativa pronta para stakeholders.

## Quando usar
- Quando você precisa priorizar um backlog e justificar cada decisão com dados
- Quando precisa apresentar um roadmap para stakeholders sem se comprometer com datas fixas
- Quando quer conectar cada item do roadmap a um job real do usuário ou OKR do trimestre
- Quando precisa alinhar time, liderança e stakeholders em torno de uma visão única de produto

## Inputs esperados
```json
{
  "product_context": "Descrição do produto e momento atual",
  "okrs": [
    {"objective": "O objetivo", "key_results": ["KR1", "KR2"]}
  ],
  "opportunities": [
    {"title": "Nome da oportunidade", "user_job": "Job relacionado", "evidence": "Evidência"}
  ],
  "constraints": {
    "team_size": "Ex: 2 devs, 1 designer",
    "timeline": "Ex: Q2 2026",
    "current_stage": "Ex: growth / early-stage / maturity"
  }
}
```

## Outputs
Markdown estruturado com: Prioritization Scoring, Roadmap Now/Next/Later conectado a OKRs e Jobs,
justificativa de cada decisão, itens descartados com motivo e narrativa para apresentação a stakeholders.

## Frameworks utilizados
- **Now/Next/Later:** Roadmap agnóstico sem datas, focado em horizontes de confiança
- **Opportunity Roadmap (Teresa Torres):** Cada item conectado a uma oportunidade da OST validada
- **JTBD Roadmap:** Priorização baseada nos jobs funcionais, emocionais e sociais do usuário
- **OKR-driven Roadmap:** Cada item justificado pelo impacto em Key Results mensuráveis

## Como usar
1. Descreva o contexto atual do produto (stage, mercado, momento)
2. Forneça os OKRs do período (objetivo + key results)
3. Liste as oportunidades identificadas na discovery com evidências
4. Informe as restrições reais de time e prazo
5. Execute o agente e use o roadmap gerado como base para alinhamento com stakeholders

## Exemplo real
**Produto:** App de gestão financeira para freelancers MEI brasileiros
**OKR:** Aumentar retenção de 30 dias de 23% para 50% no Q2 2026
**Resultado:** O agente gerou um roadmap Now/Next/Later com 3 itens no Now priorizados pelo
job "controlar DAS sem precisar de contador", justificativa para cada decisão e descartou
2 features que não conectavam a nenhum OKR ou job mapeado
