# PM Validation Agent

## O que faz
Estrutura o processo de design de testes para validar hipóteses de produto antes de investir em desenvolvimento. Funciona de forma agnóstica para qualquer produto, mercado ou audiência, aplicando o Lean Testing + Experimentation Framework para recomendar a metodologia de teste mais adequada, critérios de sucesso e plano de execução.

## Quando usar
- Antes de iniciar o desenvolvimento de uma nova feature ou produto
- Quando você tem uma hipótese sobre comportamento de usuário que precisa ser validada
- Quando precisa justificar decisões de produto com dados antes de alocar recursos

## Inputs esperados
```json
{
  "hypothesis": "Acreditamos que [segmento] vai [comportamento] porque [razão]",
  "target_audience": "Descrição do perfil do usuário a ser testado",
  "constraints": {
    "timeline": "Ex: 2 semanas",
    "budget": "Ex: R$ 500",
    "resources": "Ex: 1 PM, acesso a base de 200 usuários"
  }
}
```

## Outputs
Markdown estruturado com: metodologia de teste recomendada, tamanho de amostra, critérios de sucesso mensuráveis, timeline detalhado, recursos necessários e avaliação de riscos.

## Como usar
1. Forneça sua hipótese no formato "Acreditamos que X vai Y porque Z"
2. Descreva quem é o público-alvo do teste com o máximo de especificidade
3. Liste suas restrições reais de prazo, orçamento e recursos disponíveis
4. Execute o agente e revise o plano de teste gerado
5. Ajuste os critérios de sucesso conforme o contexto do seu produto

## Exemplo real
**Hipótese:** Freelancers brasileiros que faturam entre 30-100k/ano abandonam ferramentas de controle financeiro porque o processo de categorização manual é demorado demais.

**Resultado:** O agente recomendou 8 entrevistas qualitativas + diary study de 5 dias com critério de sucesso: ≥6/8 usuários relatam >15 min/semana gastos em categorização manual.
