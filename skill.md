# skill.md — PM-builder

## Visão Geral

O **PM-builder** é uma coleção de agentes de IA especializados em Product Management. Cada agente estrutura uma etapa crítica do ciclo de vida de produto, desde a discovery até a priorização e validação de hipóteses.

---

## Agentes disponíveis

### 1. PM Discovery Agent
**Arquivo:** `agents/pm-discovery-agent/`

**O que faz:**
Estrutura o processo de discovery e desk research combinando Continuous Discovery Habits (Teresa Torres), JTBD e Opportunity Mapping. Constrói uma Opportunity Solution Tree, mapeia jobs reais dos usuários, identifica gaps de mercado e gera insights acionáveis antes do desenvolvimento.

**Frameworks:**
- Continuous Discovery Habits (Teresa Torres) — Desired outcome, OST, assumption mapping
- JTBD (Jobs To Be Done) — Functional, emotional e social jobs no formato "When / I want / So I can"
- Secondary Research + Opportunity Mapping — Desk research em fontes públicas

**Inputs:**
| Campo | Tipo | Descrição |
|---|---|---|
| `product_description` | string | O que está sendo explorado |
| `target_audience` | string | Perfil do usuário-alvo |
| `research_goal` | string | Pergunta central da pesquisa |
| `available_resources` | object | Tempo, ferramentas, dados existentes |

**Output:** Markdown com Desired Outcome, OST, User Jobs, Pain Points, Market Gaps, Competitive Landscape, Assumption Mapping e Discovery Cadence.

---

### 2. PM Roadmap Agent
**Arquivo:** `agents/pm-roadmap-agent/`

**O que faz:**
Estrutura e prioriza roadmaps de produto combinando Now/Next/Later, Opportunity Roadmap (Teresa Torres), JTBD Roadmap e OKR-driven prioritization. Gera um roadmap justificado com narrativa pronta para stakeholders.

**Frameworks:**
- Now/Next/Later — Roadmap agnóstico sem datas, focado em horizontes de confiança
- Opportunity Roadmap (Teresa Torres) — Cada item conectado a uma oportunidade da OST validada
- JTBD Roadmap — Priorização por jobs funcionais, emocionais e sociais
- OKR-driven Roadmap — Cada item justificado pelo impacto em Key Results

**Inputs:**
| Campo | Tipo | Descrição |
|---|---|---|
| `product_context` | string | Descrição do produto e momento atual |
| `okrs` | array | Objetivos e Key Results do período |
| `opportunities` | array | Oportunidades identificadas na discovery |
| `constraints` | object | Tamanho do time, prazo, estágio atual |

**Output:** Markdown com Prioritization Scoring, Roadmap Now/Next/Later conectado a OKRs e Jobs, justificativa de cada decisão, itens descartados com motivo e narrativa para apresentação.

---

### 3. PM Validation Agent
**Arquivo:** `agents/pm-validation-agent/`

**O que faz:**
Estrutura o design de testes para validar hipóteses de produto antes de investir em desenvolvimento. Aplica o Lean Testing + Experimentation Framework para recomendar a metodologia de teste mais adequada, critérios de sucesso e plano de execução.

**Framework:**
- Lean Testing + Experimentation Framework

**Inputs:**
| Campo | Tipo | Descrição |
|---|---|---|
| `hypothesis` | string | "Acreditamos que X vai Y porque Z" |
| `target_audience` | string | Perfil do usuário a ser testado |
| `constraints` | object | Prazo, orçamento, recursos disponíveis |

**Output:** Markdown com metodologia de teste recomendada, tamanho de amostra, critérios de sucesso mensuráveis, timeline, recursos e avaliação de riscos.

---

## Fluxo recomendado

```
Discovery → Roadmap → Validation
     ↓            ↓           ↓
       OST + Jobs   Priorização  Teste de
         mapeados     por OKR      hipóteses
         ```

         1. **PM Discovery Agent** — mapeie oportunidades e jobs antes de qualquer código
         2. **PM Roadmap Agent** — priorize as oportunidades conectando a OKRs e jobs validados
         3. **PM Validation Agent** — teste hipóteses específicas antes de alocar o time de dev

         ---

         ## Estrutura do repositório

         ```
         PM-builder/
         ├── README.md
         ├── skill.md
         └── agents/
             ├── pm-discovery-agent/
                 │   ├── README.md
                     │   ├── agent.json
                         │   └── example_input.json
                             ├── pm-roadmap-agent/
                                 │   ├── README.md
                                     │   └── agent.json
                                         └── pm-validation-agent/
                                                 ├── README.md
                                                         └── agent.json
                                                         ```

                                                         ---

                                                         ## Como adicionar um novo agente

                                                         1. Crie uma pasta em `agents/nome-do-agente/`
                                                         2. Adicione um `agent.json` com os campos: `name`, `version`, `description`, `tags`, `framework`, `inputs`, `output_format`
                                                         3. Adicione um `README.md` com: o que faz, quando usar, inputs esperados, outputs e exemplo real
                                                         4. Documente a skill aqui no `skill.md`
