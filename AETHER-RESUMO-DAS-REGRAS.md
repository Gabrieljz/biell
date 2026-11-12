# Trabalho AETHER — "Live Voice Conversation Ranking" (resumo em português)

Resumo de estudo feito a partir das 43 fotos das regras e do vídeo de explicação (11/11/2026).
Plataforma: multimango.com — tarefa `260310-live-s2s-elo` — tela "Live S2S Arena".
Não foram fotografadas as abas **Walkthrough**, **QA Rubric** e **Assessment**.

---

## 1. O que é o trabalho

Você conversa **por voz, ao vivo, em inglês** com dois modelos (Modelo A e Modelo B), usando o **mesmo cenário**,
e depois diz qual conversa foi melhor, com provas do que você ouviu.

- **Estrela-guia (North Star):** um chatbot que fala como um amigo inteligente e carismático: natural, útil,
  correto e fácil de acompanhar. Não um sistema lendo resposta pronta.
- **Persona:** às vezes o cenário pede que o modelo faça um personagem (voz, tom, emoção, idade/gênero percebidos,
  personalidade). Aí você avalia se o personagem ficou consistente e convincente.
- **Vá pelo instinto:** o primeiro e mais importante julgamento é a preferência geral:
  *"Como usuário, com qual modelo eu ia querer conversar de novo nesse tipo de pedido?"*
- **Regra padrão:** se os dois são parecidos, naturalidade e engajamento decidem — **mas só depois** de a
  informação estar razoavelmente correta (sem coisa inventada ou erro que atrapalhe o objetivo do cenário).

## 2. Passo a passo (SOP)

### 2.1 Antes de começar
1. Leia o cenário do começo ao fim. Anote o objetivo e as condições (orçamento, quantidade de itens, emoção,
   "o modelo não deve dar conselho, só ouvir" etc.).
2. Olhe a parte **"Skills Tested"**: ela diz o que o cenário está testando.
3. **Decida o plano:** como você começa e como vai "apertar" o modelo (uma pergunta a mais, uma correção, uma
   interrupção). O **mesmo plano vale para os dois modelos**.
4. Os dois modelos recebem a mesma atenção, esforço e contexto. O número de turnos deve ficar o mais parecido possível.

### 2.2 Prioridades (o que pesa mais)
- **Padrão:** Naturalidade > Utilidade > Qualidade do áudio.
- **Cenário EQ (emocional):** Naturalidade/Engajamento > Utilidade > Áudio.
- **Cenário IQ (informação):** Utilidade > Naturalidade/Engajamento > Áudio.
- **Endpointing (dinâmica da conversa):** o que importa é a troca de turnos: quando falar, ouvir, ceder, interromper.
- **Híbrido:** use a pergunta-âncora: *"O que o usuário queria tirar dessa conversa?"*
- Exemplo das regras: A é mais simpático, mas dá uma resposta errada com confiança em algo importante; B é menos
  polido, mas certo → **ganha o B**.
- Uma **falha catastrófica** em qualquer dimensão pode pesar mais do que a ordem normal.

### 2.3 Falando com os modelos
1. **Interprete o cenário.** Nada de conversa aleatória.
2. **Vários turnos.** Uma troca só não basta; é no vai e volta que o modelo quebra.
3. Regras enquanto fala:
   - **Scenario Adherence (ficar na tarefa):** siga o cenário exatamente. Não traga assunto de fora, não ignore as
     condições, não teste o modelo aleatoriamente.
   - **Scenario Coherence (fazer sentido / igualdade):** seu comportamento tem que ser lógico e parecido nos dois
     modelos. Não se contradiga (ex.: dizer que o orçamento é curto e depois reclamar que a resposta é barata), não dê
     perguntas fáceis pra um e difíceis pro outro.
   - **No Scripting (sem roteiro):** fale ao vivo, natural. **Nunca leia texto pronto** nem siga um roteiro ensaiado.
     O certo: anotar o objetivo e 1 ou 2 assuntos, e deixar cada fala responder ao que o modelo disse.
   - **No Bad-faith (boa-fé):** não tente quebrar, enganar ou sabotar o modelo. Não ler roteiro, não ler o texto do
     cenário sem mudar, não deixar música ou TV no fundo, **não usar modificador/sintetizador de voz nem IA (LLM)
     para fazer a tarefa**. Isso é falha catastrófica: **banimento imediato** da plataforma.

### 2.4 Avaliar as dimensões
| Dimensão | Opções | O que mede |
|---|---|---|
| **Overall Preference** (a mais importante) | A / B | Preferência total pela experiência; depende muito do tipo de cenário. |
| **Naturalness / Engagement / Aesthetics** | A / B | Soou humano? Conversa envolvente, como com um amigo? Entrega autêntica? Ritmo, tom, presença emocional. Cuidado com fala robótica, repetição, "reinícios" e **turn-hoarding** (domina e não deixa você falar). |
| **Utility** | A / B / Empate (ambos bons) / Empate (ambos ruins) | Só a informação: correta, relevante, específica, dá pra agir? Não entra tom nem se seguiu instruções. Resposta errada com confiança perde pra um honesto "não tenho certeza, mas…". |
| **Audio Quality** | A / B / Both good / Both bad | Só a estética do som: travadas, falhas, estalos, "warbling" etc. |
| **Conversational Dynamics** | A / B / empate / (skip) | Troca de turnos respeitosa, escuta ativa, pausas, interrupções, "uh-huh", "right". |
| **Task Success** | Pass / Fail (na tela também tem Partial), por modelo | O modelo atendeu **todos** os pedidos, explícitos **e** implícitos, no registro emocional certo? Se o usuário só queria desabafar e o modelo deu conselho = **falha**, mesmo que o conselho seja bom. |

Nas subdimensões, procure diferenças **sutis, mas inequívocas**.

### 2.5 Qualidade do áudio (aprofundado)
- Avalie **só o áudio do modelo**. Nunca o seu microfone, seu ruído de fundo ou seu teclado.
- **Passo 1 — cada modelo sozinho:** ele tem um problema de áudio claro, que um ouvinte notaria e acharia
  incômodo? Pese **gravidade × frequência**.
- **Sempre é "problema claro" (Major):** (1) palavras que não dá pra entender de jeito nenhum (abafado mas
  compreensível não conta); (2) ruído de fundo tão alto quanto a voz, ou mais; (3) uma segunda voz aparece junto.
- Problema quase imperceptível **não conta** e não pode decidir a escolha.
- **Passo 2 — quantos têm problema claro?**
  - Nenhum → **Both good**.
  - Só um → prefira o **limpo**.
  - Os dois → prefira o **menos ruim**; se nenhum é claramente pior → **Both bad**.
- "Preferred" quer dizer só "relativamente melhor". Se os dois são ruins, escreva isso na justificativa
  ("A preferred — both bad, A less severe").

### 2.6 Lista de erros (Error Clusters)
Depois das dimensões, marque quais erros apareceram em cada modelo. Erro fora da lista vai escrito na justificativa.

**Erros do modelo**
| # | Erro | Leve (Min) | Moderado (Mod) | Grave (Maj) | Catastrófico |
|---|---|---|---|---|---|
| 1 | **Looping / LLMism** (repete frase, bordão, bajulação) | repetição sutil | repete 3–5 vezes, ignora redirecionamento | repetição incessante e incoerente | laço que não quebra |
| 2 | **Interrupted User** (corta você) | 1 vez, leve | 2–3 vezes, ou 1 vez agressiva | 4+ turnos, você não consegue terminar | — |
| 3 | **Model Refusal** (não faz o que foi pedido) | esquece um detalhe | atende só por cima / em parte | ignora ou contradiz o pedido | — |
| 4 | **Inaccuracy** (informação errada/inventada) | erro pequeno, não engana | erro num ponto importante | inventa com confiança em assunto crítico | — |
| 5 | **Anthropomorphism** (fala como se fosse humano) | 1ª pessoa leve ("eu acho…") | diz ter memórias/vivências | finge ser humano o tempo todo | — |
| 6 | **Overacted** (exagero na voz) | um pouco expressivo demais | exagerado em vários turnos | teatral, caricato | — |
| 7 | **Bad ASR / Misunderstanding** (entendeu errado) | 1 palavra, sentido se recupera | palavras-chave em 1–2 turnos | 3+ turnos | causa dano real |
| 8 | **Latency** (demora) | 1–3 s | 4–8 s | 9+ s | — |
| 9 | **Failed Correction** (não aceita correção) | se corrige depois de 1 aviso | diz que entendeu, mas continua errando | ignora totalmente | — |
| 10 | **Not Locally Relevant** (só i18n) | 1 referência de fora | várias | resposta toda baseada em outro país | — |
| 11 | **Wrong Language** | 1–2 palavras | 1 vez, corrige após 1 aviso | precisa de mais de 1 aviso | nunca usa a língua certa |
| 12 | **Wrong Gender** (só i18n) | voz feminina se refere no masculino (ou o contrário) | troca de voz no meio | erra o gênero do usuário | — |

**Erros do avaliador (é isso que a auditoria cobra de você)**
| # | Erro | Como é medido |
|---|---|---|
| 13 | **Scenario Adherence** | Min: foge de 1 requisito pequeno · Mod: ignora 2–3 · Maj: ignora a maioria |
| 14 | **Scenario Coherence** | Min: pequena diferença de esforço · Mod: desequilíbrio visível · Maj: assimetria clara |
| 15 | **Non-Spontaneous / Scripting** | Mod: turnos claramente pré-planejados · Maj: conversa escrita do começo ao fim · Cat: diálogo inteiro redigido antes e "encenado" |
| 16 | **Adversarial** | **Cat:** burlar o sistema, ex.: **usar IA (LLM) para gerar respostas ou conversas** |
| 17 | **Wrong Language from User** | Min: 1–2 deslizes · Maj: vários turnos na língua errada |
| 18 | **Missing Audio** | áudio faltando/cortado (modelo ou usuário) |
| 19 | **Other** | o que não se encaixa nos outros |

### 2.7 Quando pular
- **Skip:** o cenário não está em inglês (avise o PM se repetir) ou você não tem o conhecimento necessário.
- **Skip (Technical Issue):** o modelo trava no meio, não responde, não conecta, ou outro (inclui resposta
  insegura/nociva). Escolha o motivo certo.
- Travou por mais de **20–30 segundos** e não voltou = problema técnico (pular), **não** é "latência".
- Nunca "termine" a tarefa dando a pior nota pro lado que travou: isso contamina a comparação.

## 3. Justificativa (Rationale)

Tem que explicar suas decisões pra alguém que **não ouviu** os áudios.

> "Say what you heard. Say when you heard it. Say why it mattered."
> (Diga o que ouviu. Diga quando ouviu. Diga por que importou.)

**Modelo das regras:**
`I chose [Model] because [dimension] was stronger. At [timestamp/turn], it [observable behavior], which mattered
because [impact on user/listener]. The other model [trade-off or weakness].`

**Antes de escrever, pergunte:** 1) Qual foi o fator decisivo? 2) Onde (minuto, turno ou frase)?
3) Teve troca? O que o outro modelo fez melhor?

**A justificativa precisa:**
- Ter prova: dimensão que decidiu + minuto/turno/frase.
- Bater com o que você marcou (se marcou B no áudio, o texto não pode dizer que A tem o melhor áudio).
- Ser clara e detalhada.
- **Explicar a escolha de Audio Quality e cada Error Cluster marcado** (o que foi e onde aconteceu em cada modelo).
- "Tie Both Good": justificativa dessa nota é opcional.

**Estrutura:** O que aconteceu? → Onde/quando? → Por que importa? → E o outro modelo?

**Vago x específico (exemplos das regras):**
| Vago demais | O que eles querem |
|---|---|
| "Model B was more natural overall." | "At 0:45, B laughed and asked a follow-up. A paused 2 seconds then gave a flat 'okay, got it.'" |
| "Both had good audio quality." | "Both clean. A had minor sibilance at 0:12 and 0:34; B had a tick at 0:08 — neither worth penalizing." |
| "Model A followed instructions better." | "User asked for 3 restaurants with prices. A delivered all 3. B only covered 2 and skipped pricing." |
| "I preferred A — it sounded better." | "User was venting. A slowed pacing and dropped pitch at 0:22–0:30 — felt like listening. B stayed upbeat, which felt tone-deaf." |

**"Golden example" (o mínimo esperado):** uma linha de Audio Quality com os erros e os turnos, uma linha de Error
Cluster (ex.: 2 latências, turnos 3 e 5, 5+ s), uma de Utility comparando A e B, e a preferência geral ligada às dimensões.

**Justificativa fraca:** uma linha só, sem dimensão, sem turno, sem observação de áudio.

## 4. A tela (vídeo de explicação)

- Etapas no topo: **1. Model A → 2. Model B → 3. Vote**.
- Botões: **Skip (Technical Issue)**, **Redo** (apaga o Modelo A e grava de novo), **Done with A, switch to B**.
- Cada cenário mostra: tipo (ex.: "Practical Utility"), foco (ex.: "IQ-focused · Prioritize Utility"), tamanho
  (Short), idioma (Needs: English) e tempo máximo (ex.: max 5m). "Please speak in English."
- **WHAT TO DO** = o que fazer; **SKILLS TESTED** = o que está sendo testado; **Notes** = suas anotações.
- Lembrete da tela: tenha a **mesma conversa** com os dois (mesma abertura, mesmas perguntas, mesmo assunto). Os
  modelos respondem diferente e a conversa se afasta um pouco; tudo bem, mas quanto mais parecido o seu lado, mais
  fácil julgar.
- Instruções fixas da tela: conversa natural; fique no papel; mesma energia, assuntos, profundidade e duração nos
  dois; diferenças sutis mas inequívocas; use a prioridade do cenário; **Task Success é passa/não passa** (falha se o
  objetivo não foi atingido ou teve erro catastrófico).
- Exemplo do vídeo ("Unit & Measurement Conversion"): pedir 3 conversões em voz alta, uma por vez (250 g de farinha
  em xícaras; 60 mph em km/h; 98,6 °F em °C) e ver se o número está certo, se o modelo avisa que gramas→xícaras
  depende do ingrediente, e se fala os números com clareza.
- Tela de voto: linha do tempo com os áudios, caixa de justificativa, "Automated factuality guidance" (só ajuda, não
  decide), as dimensões, Task Success (Pass / Fail / Partial) e Error Clusters.
- **External Model:** em algumas tarefas um dos lados é um modelo de fora (no vídeo: demo web da Sesame, voz "Maya").
  Você conversa lá, grava a conversa inteira (sua voz + a do modelo) e envia um único arquivo de áudio.

## 5. Perguntas de fixação (das próprias regras)

- Qual julgamento vem primeiro? → A preferência geral.
- O que é naturalidade? → Ritmo, tom, presença emocional, troca de turnos e entrega com cara de humano.
- O que é utilidade? → Resposta correta, relevante, específica e útil pro objetivo.
- O que é dinâmica da conversa? → Escuta, troca de turnos respeitosa, interrupções, pausas e ritmo do vai e volta.
- O que é task success? → Todo pedido explícito e implícito atendido, inclusive "só me ouve".
- Fiz 3 perguntas difíceis pro A e encerrei o B depois de 1 fácil. Posso avaliar? → **Não.** Mesma atenção e
  dificuldade pros dois.
- Um modelo nunca conecta. O que fazer? → **Skip (Technical Issue)** com o motivo certo.
