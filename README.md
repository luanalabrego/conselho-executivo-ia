# Conselho Executivo IA

Seu conselho executivo pessoal, movido por inteligencia artificial.

6 executivos C-level com personalidades distintas debatem suas pautas, analisam dados da sua empresa e ajudam voce a tomar decisoes estrategicas fundamentadas.

---

## O Que E

O Conselho Executivo IA e um framework que simula um conselho de administracao completo dentro do Claude Code. Cada conselheiro tem uma especialidade, uma forma de pensar e um conjunto de ferramentas para analisar problemas sob sua perspectiva.

Eles debatem entre si, levantam riscos que voce nao viu, questionam premissas e documentam tudo.

---

## Seus Conselheiros

| Conselheiro | Nome | Especialidade | O Que Ele Faz Por Voce |
|-------------|------|---------------|----------------------|
| CEO | Victor (Visionario) | Estrategia e visao | Define o norte, prioriza, decide em impasses |
| CFO | Helena (Guardia) | Financas | Analisa viabilidade, projeta cenarios, protege o caixa |
| COO | Rafael (Engrenagem) | Operacoes | Mapeia processos, identifica gargalos, planeja execucao |
| CMO | Marina (Amplificadora) | Marketing | Posiciona marca, planeja aquisicao, otimiza funil |
| CCO | Caio (Ponte) | Clientes | Traz a voz do cliente, analisa retencao, protege experiencia |
| CRO | Rodrigo (Acelerador) | Receita e Vendas | Constroi maquina de vendas, projeta receita, acelera pipeline |

---

## Como Funciona

1. **Voce traz uma pauta** — Ex: "Devo contratar um vendedor ou investir em trafego pago?"
2. **Cada C-level analisa** sob sua perspectiva com dados da sua empresa
3. **Eles debatem** — com contrapontos obrigatorios e riscos levantados
4. **O CEO sintetiza** e conduz a decisao
5. **Tudo e documentado** — decisao, votos, acoes, KPIs, data de revisao

---

## Comece em 3 Passos

### Passo 1 — Instalar

Instale o Claude Code CLI (precisa de Node.js):

```bash
npm install -g @anthropic-ai/claude-code
```

Configure sua chave da API Anthropic:

```bash
claude config set apiKey sk-ant-SUA-CHAVE-AQUI
```

(Crie sua chave em https://console.anthropic.com)

### Passo 2 — Abrir

Navegue ate esta pasta e inicie:

```bash
cd council-package
claude
```

### Passo 3 — Onboarding

Na primeira vez, configure sua empresa:

```
*onboarding
```

Responda 6 perguntas sobre sua empresa. Depois disso, todos os conselheiros conhecem seu negocio.

---

## Exemplos de Uso

### Reuniao do Conselho
```
*reuniao Definir estrategia de pricing para o proximo trimestre
```

### Debate Especifico
```
*debate Vale a pena investir R$ 10K em trafego pago agora?
```

### Conversar com um Conselheiro
```
/council/cfo Preciso analisar se tenho caixa para contratar 2 pessoas
```

### Briefing Executivo
```
*briefing
```

---

## Estrutura de Pastas

```
council-package/
├── CLAUDE.md                    # Cerebro do conselho (instrucoes da IA)
├── SETUP.md                     # Guia de instalacao
├── ONBOARDING.md                # Configuracao inicial
├── README.md                    # Este arquivo
├── constitution.md              # 5 principios inviolaveis
├── .claude/commands/council/    # Slash commands dos agentes
├── agents/                      # Definicoes completas dos 7 agentes
├── templates/                   # Templates de ata, decisao, briefing
└── data/
    ├── empresa/                 # Dados da SUA empresa (alimente aqui)
    ├── decisoes/                # Decisoes salvas automaticamente
    ├── reunioes/                # Atas salvas automaticamente
    └── memoria/                 # Sistema de memoria do conselho
```

---

## Alimentando Dados

Quanto mais dados voce colocar em `data/empresa/`, melhores as recomendacoes.

Exemplos do que adicionar:
- **DRE ou fluxo de caixa** (a Helena agradece)
- **Metricas de marketing** — CAC, LTV, funil (a Marina precisa)
- **Dados de clientes** — NPS, churn, feedback (o Caio usa)
- **Pipeline de vendas** — deals, forecast (o Rodrigo vive disso)
- **Metricas operacionais** — SLAs, entregas (o Rafael quer)

Formatos: `.md`, `.txt`, `.csv`, `.json`, `.yaml`

---

## Os 5 Principios do Conselho

1. **Decisao Baseada em Dados** — Sem dados, sem decisao
2. **Debate Antes de Decidir** — Todo tema passa pelo conselho completo
3. **Transparencia Total** — Tudo documentado, nada off the record
4. **Autoridade por Dominio** — Cada C-level manda no que e seu
5. **Voto de Minerva** — O CEO desempata, com justificativa

---

## Preco

**Gratuito.**

O unico custo e o uso da API da Anthropic (Claude). Uma sessao tipica custa entre US$ 0.50 e US$ 2.00.

---

## Duvidas

Se tiver problemas na instalacao, consulte o arquivo `SETUP.md` para instrucoes detalhadas e solucao de problemas comuns.

---

*Conselho Executivo IA v1.0 — Seu conselho, suas decisoes, seus dados.*
