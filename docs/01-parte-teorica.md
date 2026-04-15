# Parte Teórica — CalmAI: Diário Emocional com Inteligência Artificial

> **Disciplina:** Metodologias Ágeis e Validação de Produtos — UniFECAF
> **Entregável 1 (1,5 pontos)** — Análise e Discussão
> **Produto validado:** CalmAI

---

## 1.1 Problema e Oportunidade

### Problema real identificado

Jovens brasileiros entre 18 e 30 anos enfrentam um nível crescente de ansiedade, estresse e burnout, mas **não têm uma ferramenta acessível, privada e contínua para entender seus próprios padrões emocionais**. As alternativas atuais se dividem em três grupos insuficientes:

1. **Apps de meditação genéricos** (Headspace, Lojong, Calm) — entregam conteúdo padronizado, sem personalização real e sem entender o contexto da pessoa.
2. **Terapia digital paga** (Cíngulo, Zenklub, Vittude) — eficaz, mas custa entre R$30 e R$200/mês, fora do orçamento da maioria dos jovens em início de carreira.
3. **Diários tradicionais (papel ou apps simples)** — exigem disciplina alta e não geram insight: o usuário escreve, mas não enxerga padrões nem evolução.

A consequência é uma lacuna: a pessoa **sente** que algo está errado, mas não consegue **mapear** quando, com que frequência, em que contextos, ou como evolui ao longo do tempo. Isso atrasa a busca por ajuda profissional e perpetua ciclos de sofrimento silencioso.

### Público-alvo

**Persona principal — "Marina, a estudante-trabalhadora"**

| Atributo | Descrição |
|---|---|
| Idade | 22 anos |
| Ocupação | Universitária (4º semestre) e estagiária |
| Renda | R$1.500 a R$3.500/mês |
| Comportamento digital | Usa Instagram, TikTok, ChatGPT diariamente; conhece IA mas não se considera "tech" |
| Dor central | Ansiedade recorrente, dificuldade de dormir, sensação de "estar sempre atrasada na vida" |
| Já tentou | Conversar com amigos (vergonha), terapia (caro), Headspace (não engajou) |
| Disposta a pagar | Até R$25/mês se entregar valor real e mensurável |

**Personas secundárias:**
- **Diego, 27, dev em transição de carreira** — burnout silencioso, não se reconhece como "alguém que precisa de ajuda".
- **Bia, 19, primeiro semestre da faculdade longe de casa** — solidão e crises de ansiedade noturnas.

### Impacto do problema no mercado

| Indicador | Valor | Fonte |
|---|---|---|
| Brasileiros com transtorno de ansiedade | ~18,6 milhões (8,9% da pop.) | OMS, 2024 |
| Crescimento de ansiedade em jovens 18-29 pós-pandemia | +25% | FioCruz, 2023 |
| Brasileiros com depressão diagnosticada | 16,3 milhões | IBGE PNS, 2019 |
| Tamanho do mercado global de mental health apps | US$ 6,2 bi (2024) → US$ 17,5 bi (2030) | Grand View Research |
| Profissionais de psicologia no SUS por 100k habitantes | 2,1 (vs ideal de 10) | CFP, 2023 |

> A combinação de **demanda crescente** + **oferta pública insuficiente** + **alto custo da oferta privada** cria uma janela clara para uma solução acessível, escalável e orientada por dados que NÃO substitui terapia, mas reduz a barreira inicial de auto-conhecimento.

---

## 1.2 Ideação com IA

> Documento detalhado em [`05-ideacao-com-ia.md`](./05-ideacao-com-ia.md). Resumo abaixo.

### Ferramentas utilizadas

| Ferramenta | Papel |
|---|---|
| **Claude (Opus 4.6)** | Brainstorm divergente, estruturação de hipóteses Lean, análise crítica de viabilidade |
| **ChatGPT (GPT-4)** | Mapeamento de concorrentes, geração de personas, validação cruzada |
| **Gemini (2.5 Pro)** | Pesquisa de dados de mercado e estatísticas oficiais |
| **Perplexity (Sonar Pro)** | Verificação de fontes citadas (anti-alucinação) |

### Como a IA ajudou a gerar e aprimorar ideias

A IA foi usada como **co-piloto, não autopiloto**, em 3 momentos:

1. **Divergência (5 min)**: prompt no Claude gerou 10 ideias de produtos baseados em IA atacando dores reais de jovens 18-30. Sem IA, esse brainstorm levaria 2-3 horas sozinho.
2. **Convergência (15 min)**: matriz de critérios (dor real, acessibilidade do público, defensibilidade vs IA genérica, monetização, risco ético) aplicada em conjunto com a IA para reduzir 10 → 3.
3. **Refinamento (30 min)**: ChatGPT mapeou concorrentes e identificou o gap competitivo; Gemini trouxe estatísticas oficiais que validaram o tamanho do problema.

### Alternativas consideradas (e por que descartadas)

| Ideia | Por que descartada |
|---|---|
| **EstudaFlash** — tutor IA para faculdade (flashcards + revisão espaçada) | Mercado saturado (Quizlet, Anki, Notion AI). Diferencial fraco. |
| **EntrevistaPro** — simulador de entrevista de emprego com IA | Dor sazonal, público restrito, Pramp/Interviewing.io já cobrem o nicho técnico. |
| **CardápioAI** — plano alimentar personalizado para nutricionistas | Modelo B2B exige ciclo de venda longo, incompatível com 5 entrevistas. |
| **ContrataAI** — triagem de currículos para PMEs | Tema "RH com IA" altamente regulado (LGPD, viés algorítmico). Risco alto. |

**Ideia escolhida: CalmAI** — combinação única de dor crescente, público acessível para validar, diferencial real (análise temporal + privacidade + PT-BR) e narrativa de pitch emocionalmente forte.

### Limites observados ao usar IA

- IA inventou uma estatística no primeiro draft — exigiu verificação manual em fontes primárias.
- IA tendia a acrescentar features sem critério — disciplina de MVP teve que vir do humano.
- Tom de voz para saúde mental ficou inicialmente clínico demais — calibração humana foi necessária.

---

## 1.3 Hipóteses do Produto

Hipóteses formuladas no padrão **Lean Startup** ("Acreditamos que X. Saberemos que é verdade quando Y").

### Hipótese de Problema

> **Acreditamos que** jovens entre 18 e 30 anos sentem ansiedade frequente mas não conseguem mapear seus próprios padrões emocionais ao longo do tempo, e que essa ausência de auto-conhecimento contribui para a sensação de falta de controle.
>
> **Saberemos que é verdade quando** ≥ 70% dos respondentes da pesquisa relatarem que (a) sentem ansiedade pelo menos 1x por semana E (b) não usam nenhum método sistemático para acompanhar como se sentem ao longo do tempo.

### Hipótese de Solução

> **Acreditamos que** um diário digital onde o usuário escreve livremente como está se sentindo, e uma IA analisa o texto para identificar padrões emocionais e sugerir reflexões personalizadas, oferece valor superior a apps de meditação genéricos e a diários tradicionais.
>
> **Saberemos que é verdade quando** ≥ 60% dos respondentes marcarem nota ≥ 4 (escala 1-5) ao serem questionados sobre o interesse em usar a solução proposta após verem o protótipo.

### Hipótese de Valor

> **Acreditamos que** o público-alvo está disposto a pagar entre R$15 e R$25 por mês por uma solução que entregue (a) conversa em português natural, (b) análise temporal de padrões emocionais e (c) garantia de privacidade dos dados.
>
> **Saberemos que é verdade quando** ≥ 40% dos respondentes interessados (resposta ≥ 4 na hipótese de solução) declararem disposição de pagar pelo menos R$15/mês.

---

## 1.4 Proposta de MVP

> **MVP (Minimum Viable Product)** é a versão mínima do produto capaz de gerar **aprendizado validado** sobre o comportamento dos usuários com o **menor esforço possível**.

### Funcionalidades mínimas do MVP

| # | Funcionalidade | Descrição |
|---|---|---|
| F1 | **Entrada de diário em texto livre** | Usuário escreve como está se sentindo, sem campos rígidos |
| F2 | **Tag emocional automática (IA)** | IA classifica cada entrada em emoções primárias (alegria, ansiedade, tristeza, raiva, calma) |
| F3 | **Resumo semanal personalizado** | A cada 7 entradas, IA gera um resumo do "como você esteve essa semana" + 1 reflexão acionável |
| F4 | **Linha do tempo emocional visual** | Gráfico simples mostrando a evolução das emoções nas últimas 4 semanas |
| F5 | **Política de privacidade explícita** | Tela inicial mostrando que dados não são vendidos nem usados para treinar modelos |

### Justificativa de priorização (MoSCoW)

| Categoria | Itens | Justificativa |
|---|---|---|
| **Must have** | F1, F2, F3 | Sem entrada livre + análise IA + resumo, não há produto. É o coração da proposta. |
| **Should have** | F4 | Gráfico amplifica a percepção de valor ("eu vejo meu progresso"), mas o produto funciona sem ele no MVP inicial. |
| **Could have** | F5 (em produção) | Política existe desde o dia 1, mas a UI dedicada pode ser simplificada no MVP. |
| **Won't have (agora)** | Login com Google, integração com Apple Health, modo voz, notificações push, comunidade, exportação PDF | Adicionam complexidade sem testar a hipótese central de que pessoas escrevem e voltam. |

### O que NÃO está no MVP (e por quê)

- ❌ **Login social / OAuth** — friction desnecessária para validar uso. MVP usa apenas e-mail + senha.
- ❌ **Modo voz** — exige integração de speech-to-text que adia a validação central.
- ❌ **Comunidade / compartilhamento** — risco ético alto sem moderação madura.
- ❌ **Integrações com terapeutas** — depende de parcerias profissionais, fora do escopo de validação.

A regra de ouro foi: **toda feature precisa ajudar a testar a hipótese de que jovens escrevem com regularidade e percebem valor na análise. Tudo o mais é distração.**

---

## 1.5 Estratégia de Validação

### Experimento de validação

**Tipo:** Landing page de validação + formulário Typeform + teste de protótipo.

**Mecânica:**
1. Landing page apresenta o conceito do CalmAI com hero, demonstração visual da feature principal (linha do tempo emocional), prova social fictícia (depoimentos plausíveis sinalizados como mockup) e CTA único: "Quero participar da pesquisa".
2. CTA leva ao Typeform com 10 perguntas estruturadas para testar as 3 hipóteses.
3. Distribuição: redes sociais pessoais, grupos de WhatsApp de faculdade, comunidades de jovens.
4. Janela de coleta: 5 dias.

### Métricas de sucesso

| Métrica | Threshold para "validado" |
|---|---|
| **Taxa de cliques no CTA** (Landing → Typeform) | ≥ 30% dos visitantes |
| **Hipótese de Problema** (frequência de ansiedade + ausência de método) | ≥ 70% dos respondentes |
| **Hipótese de Solução** (interesse no produto após ver o protótipo, nota ≥ 4 de 5) | ≥ 60% dos respondentes |
| **Hipótese de Valor** (disposição de pagar ≥ R$15/mês) | ≥ 40% dos interessados |
| **NPS qualitativo** ("você recomendaria isso a um amigo?") | ≥ 50% sim |
| **Mínimo de respostas** | ≥ 5 |

### Critérios de decisão

| Cenário | Decisão |
|---|---|
| **Todas as 3 hipóteses validadas** (acima do threshold) | **SEGUIR** — desenvolver MVP funcional, planejar beta fechado com 20 usuários |
| **Hipóteses 1 e 2 validadas, mas Hipótese 3 (pagamento) falha** | **AJUSTAR** — manter ideia, pivotar modelo de monetização (ex.: freemium com features pagas, B2B em parceria com universidades) |
| **Hipótese 1 validada, mas Hipóteses 2 e 3 falham** | **AJUSTAR** — manter problema, redesenhar a solução (talvez não seja diário, talvez seja chat ativo) |
| **Hipótese 1 falha** (problema não é tão real quanto parecia) | **PIVOTAR ou ABANDONAR** — reavaliar se vale insistir em saúde mental ou migrar para outra dor identificada nas entrevistas |

### Ciclo Build → Measure → Learn aplicado

| Fase | Ação | Saída |
|---|---|---|
| **Build** | Landing + protótipo HTML + Typeform | Artefatos prontos em 2 dias |
| **Measure** | Coleta de respostas + métricas de engajamento | Dados quantitativos e qualitativos |
| **Learn** | Análise das respostas vs hipóteses + decisão fundamentada | Decisão documentada em [`03-experimento-validacao.md`](./03-experimento-validacao.md) |

A intenção é repetir esse ciclo em sprints semanais nas fases seguintes do produto (fora do escopo deste trabalho), validando uma hipótese nova a cada iteração.

---

**Próximos documentos relacionados:**
- Lean Canvas: [`02-lean-canvas.md`](./02-lean-canvas.md)
- Resultados do experimento: [`03-experimento-validacao.md`](./03-experimento-validacao.md)
- Roteiro do vídeo pitch: [`04-roteiro-video-pitch.md`](./04-roteiro-video-pitch.md)
