# CalmAI — Diário Emocional com Inteligência Artificial

> **Projeto de validação de produto digital** — Trabalho da disciplina **Metodologias Ágeis e Validação de Produtos** · UniFECAF
>
> *Da ideia ao produto validado: construindo e testando uma solução digital com métodos ágeis.*

---

## 🎬 Vídeo Pitch

▶ **[ASSISTIR (link a inserir após gravação)](https://www.loom.com/share/SUBSTITUIR-PELO-LINK)**

> Substitua o link acima pelo URL do Loom/YouTube/Drive após gravar o vídeo seguindo o roteiro em [`docs/04-roteiro-video-pitch.md`](docs/04-roteiro-video-pitch.md).

---

## 1. Problema

O Brasil é o país mais ansioso do mundo segundo a OMS (2024). Entre jovens de 18 a 29 anos, a ansiedade cresceu **25% após a pandemia** (FioCruz, 2023). E mais: essas pessoas **sentem** que algo está errado, mas não conseguem **mapear** o que é, quando acontece, ou como evolui ao longo do tempo.

As alternativas atuais falham em três frentes:

- **Apps de meditação genéricos** (Headspace, Lojong) entregam conteúdo padronizado e geram baixo engajamento (3 em 4 desistem na 1ª semana — Sensor Tower, 2023).
- **Terapia digital paga** (Cíngulo, Zenklub) custa entre R$30 e R$200/mês — fora do orçamento de quem está em início de carreira.
- **Diários tradicionais** exigem disciplina alta e não geram insight: o usuário escreve, mas não enxerga padrões.

📄 *Detalhamento completo:* [`docs/01-parte-teorica.md`](docs/01-parte-teorica.md)

---

## 2. Ideia do Produto

**CalmAI** é um diário emocional com IA onde o usuário escreve livre como está se sentindo. A IA classifica as emoções automaticamente, gera um resumo personalizado a cada semana, e mostra um gráfico da evolução emocional ao longo do tempo. Tudo em português, privado, por menos de R$1 por dia.

**Proposta de valor única:**
> *"Entenda seu emocional como você entende sua agenda."*

**Diferenciais defensáveis:**

| | Apps meditação | ChatGPT | **CalmAI** |
|---|---|---|---|
| Personalização real | ✗ | parcial | ✓ |
| Lembra de ontem | ✗ | ✗ | ✓ |
| Análise temporal | ✗ | ✗ | ✓ |
| PT-BR nativo | parcial | ✓ | ✓ |
| Privacidade radical | ? | ✗ | ✓ |
| Custo mensal | R$30+ | R$110+ | Free / R$9,90 / R$19,90 (Terapia) |

> **Atualização pós-validação:** preço Pro caiu de R$19,90 → R$9,90 após o experimento mostrar que 0% dos respondentes topavam pagar R$15+. Foi criado também um plano **Pro Terapia (R$19,90)** com exportação do histórico para o terapeuta — feature que surgiu espontaneamente nas respostas abertas.

📄 *Lean Canvas completo:* [`docs/02-lean-canvas.md`](docs/02-lean-canvas.md) · *Versão visual:* [`canvas/lean-canvas.html`](canvas/lean-canvas.html)

---

## 3. Protótipo

O protótipo é composto por **duas peças complementares**:

### 3.1 Protótipo do produto — `prototipo/app.html`

**5 telas do app CalmAI** em mockups de celular lado a lado — o "como seria o produto" para quem abre o link:

1. **Onboarding** — tela de abertura com as 3 promessas de privacidade
2. **Home/Dashboard** — saudação, prompt do dia, entradas recentes com tags emocionais
3. **Nova entrada** — prompts guiados + área de escrita livre (híbrido — guiado para quem trava, livre para quem flui)
4. **Insights semanais** — gráfico de barras 7 dias + insight em linguagem natural + tags dominantes + botão de compartilhar com o terapeuta
5. **Exportar para terapeuta** — feature exclusiva do plano Pro Terapia (surgiu espontaneamente nas respostas abertas)

📁 **Arquivo:** [`prototipo/app.html`](prototipo/app.html)

### 3.2 Landing page de validação — `prototipo/index.html`

Landing page que simula a comercialização do produto e estrutura o convite à pesquisa de validação (CTA → Typeform).

📁 **Arquivos:** [`prototipo/index.html`](prototipo/index.html) + [`prototipo/style.css`](prototipo/style.css)

### Como rodar localmente

Sem dependências — basta abrir os `.html` no navegador. Para servir via HTTP local:

```bash
# Opção 1: Python
cd prototipo
python -m http.server 5180

# Opção 2: Node (npx)
npx http-server prototipo -p 5180
```

Depois acesse `http://localhost:5180/index.html` (landing) ou `http://localhost:5180/app.html` (protótipo do produto).

### O que a landing entrega

- Hero com proposta de valor + mockup interativo do app (gráfico de emoções, entrada de diário, insight da semana)
- Bloco de problema com 3 estatísticas oficiais (FioCruz, Zenklub, Sensor Tower)
- Explicação em 3 passos de como funciona
- Tabela comparativa CalmAI × ChatGPT × Apps de meditação
- Promessa de privacidade explícita
- Depoimentos mockup (sinalizados como tal)
- Estrutura de planos (Free vs Pro)
- CTA único apontando para o Typeform de validação

📐 **Responsivo:** verificado em 375px (mobile), 768px (tablet) e 1280px (desktop).

---

## 4. Experimento Realizado

**Tipo:** Landing page de validação + Typeform com 10 perguntas estruturadas.

**Distribuição:** redes pessoais e grupos de WhatsApp da faculdade.

**Janela de coleta:** 5 dias (11 a 15 de abril de 2026).

**Funnel medido (dados reais — CSV exportado do Typeform):**

```
Cliques no CTA          ──────────────     ~12
       ↓ 42% conclusão
Respostas completas     ─────────────       5
       ↓ 100% na faixa-alvo 18-30
Análise final           ───────────         5
```

> **Limitação declarada:** amostra de 5 respostas atinge o mínimo exigido pelo trabalho mas é insuficiente para conclusões estatisticamente robustas. Os sinais aqui são **direcionais, não definitivos** — e isso já é leitura suficiente para a decisão de continuar/pivotar no estágio pré-MVP.

**Hipóteses sob teste:**

| Código | Hipótese | Threshold |
|---|---|---|
| H1 | Jovens 18-30 sentem ansiedade frequente E não usam método sistemático | ≥ 70% |
| H2 | Têm interesse alto em usar o CalmAI após ver o protótipo (nota ≥ 4 de 5) | ≥ 60% |
| H3 | Topam pagar entre R$15-R$25/mês | ≥ 40% dos interessados |

📄 *Estrutura completa do experimento:* [`docs/03-experimento-validacao.md`](docs/03-experimento-validacao.md) (Parte 1)

---

## 5. Resultados da Validação

| Hipótese | Resultado real (n=5) | Status |
|---|---|---|
| **H1 — Problema (ansiedade frequente)** | **100%** pontuaram 3-5 na escala de frequência (todos com nota ≥ 3) | ✅ **Validada com força** |
| **H1 — Problema (sem método)** | **60%** não acompanham; 20% usam apps isolados; 20% em terapia | ⚠️ **Validada parcialmente** |
| **H2 — Solução** | **60%** marcaram interesse 4-5 após ver o protótipo | ✅ **Validada no threshold** |
| **H3 — Preço** | **0%** pagariam R$15+; 40% até R$15; 60% não pagaria ou só até R$10 | ❌ **Falhou com margem** |

**NPS qualitativo:** 60% recomendariam (2 "com certeza" + 1 "provavelmente"); 40% "talvez".

**Insights críticos:**

1. 🔥 **O concorrente real é o ChatGPT, não apps de meditação.** 80% dos respondentes (4 de 5) admitiram usar IA para desabafar. Diferencial precisa ser explícito no pitch: *"ChatGPT esquece tudo. CalmAI lembra e mostra o padrão."*
2. 📊 **A feature mais valorizada NÃO é a IA — é o gráfico de evolução emocional.** 80% (4/5) marcaram "ver meu padrão emocional num gráfico" como atrativo; apenas 20% marcaram "IA identificar emoções". **Reposicionar o pitch em torno do gráfico.**
3. ✍️ **"Escrever livre" teve 0 votos como atrativo.** Significa que o MVP precisa equilibrar *entrada guiada* (prompts) + *liberdade* — o usuário não quer folha em branco, quer direção.
4. 🏥 **Pedido espontâneo: "exportar para o terapeuta".** Uma respondente em terapia relatou perder o fio entre as sessões. Promovido de "Could have" para feature **âncora do plano Pro Terapia (R$19,90)**.
5. 💰 **Preço R$19,90 é inviável nesta amostra.** Nova estrutura 3-tier: Free ilimitado / Pro R$9,90 (insights + exportação básica) / Pro Terapia R$19,90 (PDF para terapeuta + comparação entre sessões).

📄 *Análise completa com clusters qualitativos e dados brutos:* [`docs/03-experimento-validacao.md`](docs/03-experimento-validacao.md) (Parte 2)

---

## 6. Conclusões

### Decisão final: SEGUIR COM AJUSTES AGRESSIVOS

Em vez de matar a ideia ou pivotar radicalmente, os dados indicaram um **pivot tático** mantendo problema, solução e público — mas ajustando **monetização, posicionamento e feature âncora** com base nos 5 respondentes reais.

| Dimensão | Antes do experimento | Depois do experimento |
|---|---|---|
| Preço Pro | R$ 19,90/mês único | **3 tiers:** Free ilimitado · Pro R$ 9,90 · Pro Terapia R$ 19,90 |
| Feature âncora do pitch | "Diário com IA" | **"Gráfico da sua evolução emocional"** |
| Concorrente comunicado | "Apps de meditação" | **"ChatGPT esquece. CalmAI lembra."** |
| Exportação para terapeuta | Could have (v2) | **Feature premium âncora do plano Pro Terapia** |
| Modo de entrada | Escrita livre em folha em branco | **Híbrido:** prompts guiados + área livre |

### O que cada número me ensinou

- **100% de ansiedade frequente** = problema existe e é universal na amostra. Não preciso convencer ninguém que tem o problema.
- **60% sem método** = espaço real no mercado. Eles *sentem* mas não *mapeam*.
- **60% interesse 4-5** = atingiu o threshold raspando. Sinaliza que a proposta ressoa, mas precisa de mais tração narrativa — e o pivô do pitch em torno do gráfico (ao invés da IA) deve ajudar.
- **0% em R$15+** = matou a hipótese de precificação original. Sem margem de dúvida.
- **80% usam ChatGPT pra desabafar** = revelação do experimento. A *verdadeira* competição é grátis, já instalada, e esquece tudo. O diferencial "memória longitudinal" precisa ser o pitch.
- **80% querem o gráfico, 20% querem IA** = a proposta de valor estava errada. Vendíamos "IA que classifica emoções"; o usuário quer "enxergar o padrão". Reposicionar.

### Aprendizados meta sobre o processo

1. **Build → Measure → Learn em 5 dias custou R$0 e gerou aprendizado real.** Sem o experimento, a ideia teria sido construída por meses com o preço errado, o pitch errado e a feature âncora errada.
2. **A IA acelerou o mecânico** (brainstorm, mapeamento de concorrentes, busca de dados, síntese de clusters) **e me deixou tempo pro estratégico** (escolha de tema, calibração de tom, julgamento de trade-offs). Co-piloto, não autopiloto.
3. **MVP de verdade é desconfortável.** Cortar features que pareciam óbvias (login social, voz, comunidade) foi a parte mais difícil — e a mais importante.
4. **Falhas validadas valem mais que sucessos não verificados.** A hipótese de preço falhou, e a feature âncora estava errada — essas duas descobertas **valem mais que dois meses de desenvolvimento desperdiçado**.
5. **Amostra pequena ≠ aprendizado pequeno.** 5 respostas não dão significância estatística, mas dão sinais direcionais suficientes para decidir *no estágio pré-MVP*. Aumentar amostra é o próximo passo — não desculpa para adiar decisões.

---

## 📁 Estrutura do Repositório

```
trabalho-mev-validacao/
├── README.md                          ← você está aqui
├── docs/
│   ├── 01-parte-teorica.md            ← Parte Teórica (entregável 1)
│   ├── 02-lean-canvas.md              ← Lean Canvas em texto (entregável 2.1)
│   ├── 03-experimento-validacao.md    ← Setup + Resultados (2.3 + 2.4)
│   ├── 04-roteiro-video-pitch.md      ← Roteiro do vídeo (apoio ao item 3)
│   └── 05-ideacao-com-ia.md           ← Evidências dos prompts e ferramentas IA usadas
├── prototipo/
│   ├── app.html                       ← Protótipo do produto em 5 telas (entregável 2.2)
│   ├── index.html                     ← Landing page de validação (convite ao Typeform)
│   └── style.css
└── canvas/
    └── lean-canvas.html               ← Versão visual exportável em PDF (Ctrl+P)
```

---

## ✅ Cobertura dos entregáveis (7,0 pontos)

| Sub-item exigido pelo PDF | Local de entrega | Pontos |
|---|---|---|
| 1.1 Problema/Oportunidade | `docs/01-parte-teorica.md` §1 | 1,5 |
| 1.2 Ideação com IA | `docs/01-parte-teorica.md` §2 + `docs/05-ideacao-com-ia.md` | (incluso) |
| 1.3 Hipóteses do Produto | `docs/01-parte-teorica.md` §3 | (incluso) |
| 1.4 Proposta de MVP | `docs/01-parte-teorica.md` §4 | (incluso) |
| 1.5 Estratégia de Validação | `docs/01-parte-teorica.md` §5 | (incluso) |
| 2.1 Canvas | `docs/02-lean-canvas.md` + `canvas/lean-canvas.html` | 3,5 |
| 2.2 Protótipo | `prototipo/index.html` | (incluso) |
| 2.3 Experimento | Typeform + `docs/03-experimento-validacao.md` Parte 1 | (incluso) |
| 2.4 Resultados | `docs/03-experimento-validacao.md` Parte 2 | (incluso) |
| 2.5 README | este arquivo | (incluso) |
| 3 Vídeo Pitch (até 4 min) | Link no topo deste README | 2,0 |
| **TOTAL** | | **7,0** |

---

## 🔗 Referências e Fontes

- **Disciplina** — Metodologias Ágeis e Validação de Produtos · UniFECAF (aulas ao vivo)
- **Rocketseat** — [Jornada Metodologias Ágeis e Validação de Produtos](https://ftr.rocketseat.com.br/jornada/metodologias-ageis-e-validacao-de-produtos/conteudos)
- **Scrum Guide** — [scrumguides.org](https://scrumguides.org)
- **Lean Startup** — [theleanstartup.com](https://theleanstartup.com)
- **Dados de saúde mental:** OMS (2024), FioCruz (2023), IBGE PNS (2019), Sensor Tower (2023), Grand View Research (2024)

---

*Trabalho desenvolvido com auxílio de ferramentas de IA (Claude, ChatGPT, Gemini) como co-piloto de ideação, conforme detalhado em [`docs/05-ideacao-com-ia.md`](docs/05-ideacao-com-ia.md). Decisões estratégicas, calibração de tom e síntese final são humanas.*
