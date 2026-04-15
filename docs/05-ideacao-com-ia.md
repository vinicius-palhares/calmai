# Ideação com IA — Processo Detalhado

> Este documento registra o processo real de ideação assistido por IA que originou o produto **CalmAI**.
> Serve como evidência para o item **1.2 Ideação com IA** da Parte Teórica.

---

## 1. Ferramentas utilizadas

| Ferramenta | Modelo / Versão | Papel no processo |
|---|---|---|
| **Claude** | Opus 4.6 (Anthropic) | Brainstorm de ideias, estruturação de hipóteses, análise crítica de viabilidade |
| **ChatGPT** | GPT-4 (OpenAI) | Validação cruzada das ideias, pesquisa de concorrentes, geração de personas |
| **Gemini** | 2.5 Pro (Google) | Pesquisa de dados de mercado, estatísticas sobre saúde mental no Brasil |
| **Perplexity** | Sonar Pro | Verificação de fontes e estatísticas citadas |

A combinação foi intencional: cada IA tem viés/força diferente, e a triangulação reduz risco de "alucinação" em dados sensíveis (saúde mental exige números corretos).

---

## 2. Fluxo de ideação (Build → Measure → Learn no próprio processo de ideação)

### Etapa 1 — Divergência (gerar muitas ideias)

**Prompt usado no Claude:**

> "Atue como um Product Manager experiente em startups de IA. Liste 10 ideias de produtos digitais baseados em IA generativa que: (a) atacam dores reais e mensuráveis de jovens entre 18-30 anos no Brasil, (b) podem ser validadas com landing page + 5 entrevistas, (c) têm diferencial defensável vs uso direto de ChatGPT. Para cada uma, dê: problema, público, diferencial em 1 linha."

**Resultado:** 10 ideias geradas, das quais 8 sobreviveram à primeira filtragem.

### Etapa 2 — Convergência (filtrar)

Critérios aplicados:

| Critério | Peso |
|---|---|
| Dor real e frequente (não "nice to have") | 30% |
| Acessibilidade do público para validação | 25% |
| Defensibilidade vs IA genérica | 20% |
| Potencial de monetização (B2C ou B2B-light) | 15% |
| Sensibilidade ética / risco regulatório | 10% (penalidade) |

### Etapa 3 — Top 3 alternativas consideradas

#### Alternativa A — EstudaFlash (tutor IA para faculdade)
- **Problema:** estudantes universitários afogados em PDFs e slides sem método de revisão
- **Solução:** upload de material → flashcards inteligentes + revisão espaçada estilo Anki
- **Por que NÃO escolhi:** mercado já saturado (Quizlet, Anki, Brainscape, Notion AI). Diferencial fraco.

#### Alternativa B — EntrevistaPro (simulador de entrevista)
- **Problema:** pré-formandos travam em entrevistas técnicas e comportamentais
- **Solução:** simulador conversacional com feedback acionável
- **Por que NÃO escolhi:** dor sazonal (concentrada em fim de semestre), público restrito, e Pramp/Interviewing.io já cobrem o nicho técnico.

#### Alternativa C — CalmAI (diário emocional com IA) ✅ ESCOLHIDA
- **Problema:** ansiedade e burnout entre jovens 18-30 cresce 25% ao ano no Brasil; apps existentes (Cíngulo, Headspace) são caros, exigem disciplina alta e não usam IA conversacional
- **Solução:** diário onde o usuário escreve livremente, IA detecta padrões emocionais, sugere reflexões CBT-light e mostra evolução temporal
- **Por que ESCOLHI:**
  - Dor crescente e validada por dados públicos (OMS, FioCruz)
  - Público acessível (toda rede de faculdade tem alguém que se identifica)
  - Diferencial real: análise temporal + privacidade (vs ChatGPT, que esquece contexto)
  - Histórias contadas no pitch viralizam (apelo emocional alto)

---

## 3. Refinamento da ideia escolhida

Após escolher CalmAI, usei novos prompts para refinar:

**Prompt no Claude (definição de hipóteses):**

> "Para o produto CalmAI (diário emocional com IA para jovens 18-30 com ansiedade), formule 3 hipóteses no padrão Lean Startup: hipótese de problema, hipótese de solução e hipótese de valor. Cada uma deve ser falsificável com pesquisa de até 10 perguntas em formulário."

**Prompt no ChatGPT (concorrência):**

> "Liste apps de saúde mental e bem-estar emocional populares no Brasil em 2025, com modelo de negócio, público-alvo, principais críticas em reviews da App Store/Play Store. Foque em apps que usam IA."

Resposta consolidada:
- **Cíngulo:** terapia digital, R$30/mês, criticado por "scripts engessados"
- **Lojong:** meditação, freemium, criticado por "conteúdo repetitivo"
- **Wysa (internacional):** chatbot de IA, freemium, em inglês — barreira para o público BR
- **Replika:** companhia conversacional, mas posicionado como "amigo virtual", não saúde

**Gap identificado:** ninguém combina **escrita livre + IA conversacional em PT-BR + análise temporal de padrões emocionais** com privacidade explícita.

**Prompt no Gemini (validação de dados de mercado):**

> "Quais são os dados mais atuais e confiáveis sobre prevalência de transtornos de ansiedade e depressão em jovens 18-30 anos no Brasil? Cite as fontes."

Dados confirmados (com fontes — verificar em produção do doc final):
- OMS (2024): Brasil é o país mais ansioso do mundo, 9,3% da população
- FioCruz (2023): jovens 18-29 são o grupo com maior crescimento de ansiedade pós-pandemia
- IBGE PNS (2019): 16,3 milhões de brasileiros têm depressão diagnosticada

---

## 4. Como a IA realmente "ajudou" (visão honesta)

| Etapa | Sem IA levaria | Com IA levou |
|---|---|---|
| Gerar 10 ideias divergentes | 2-3 horas de brainstorm sozinho | 5 minutos |
| Comparar concorrentes | 1 dia pesquisando cada app | 10 minutos consolidado |
| Estruturar hipóteses no padrão Lean | Releitura do livro Lean Startup | 5 minutos com prompt bem feito |
| Buscar estatísticas confiáveis | Garimpo manual em sites do governo | 15 minutos com Gemini + verificação |
| Escrever copy da landing | Várias iterações sozinho | 1 prompt + 2 refinamentos |

**Limites reais observados:**
- IA inventou estatística "falsa" no primeiro draft (precisei verificar em fontes primárias)
- IA tendia a sugerir features demais — precisei aplicar disciplina de MVP manualmente
- Tom de voz para saúde mental exigiu calibração humana (IA partia para tom muito clínico)

---

## 5. Conclusão da ideação

A IA acelerou drasticamente as etapas mecânicas (divergência, comparação, estruturação) e deixou para o humano as decisões de **julgamento estratégico** (qual ideia escolher, tom de voz, ética). Esse é exatamente o uso correto de IA na fase de produto: **co-piloto, não autopiloto**.
