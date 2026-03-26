# Conselho Executivo IA

Seu conselho executivo pessoal, movido por inteligência artificial.

7 executivos C-level com personalidades distintas debatem suas pautas, analisam dados da sua empresa e ajudam você a tomar decisões estratégicas fundamentadas.

---

## O Que É

O Conselho Executivo IA é um framework que simula um conselho de administração completo dentro do Claude Code. Cada conselheiro tem uma especialidade, uma forma de pensar e um conjunto de ferramentas para analisar problemas sob sua perspectiva.

Eles debatem entre si, levantam riscos que você não viu, questionam premissas e documentam tudo.

---

## Seus Conselheiros

| Conselheiro | Nome | Especialidade | O Que Ele Faz Por Você |
|-------------|------|---------------|----------------------|
| CEO | Victor (Visionário) | Estratégia e visão | Define o norte, prioriza, decide em impasses |
| CFO | Helena (Guardiã) | Finanças | Analisa viabilidade, projeta cenários, protege o caixa |
| COO | Rafael (Engrenagem) | Operações | Mapeia processos, identifica gargalos, planeja execução |
| CMO | Marina (Amplificadora) | Marketing | Posiciona marca, planeja aquisição, otimiza funil |
| CCO | Caio (Ponte) | Clientes | Traz a voz do cliente, analisa retenção, protege experiência |
| CRO | Rodrigo (Acelerador) | Receita e Vendas | Constrói máquina de vendas, projeta receita, acelera pipeline |

---

## Como Baixar e Instalar

### Passo 1 — Baixar o Conselho

**Opção A — Download direto (mais fácil):**

1. Clique no botão verde **"<> Code"** aqui no topo desta página
2. Clique em **"Download ZIP"**
3. Descompacte o arquivo no seu computador (ex: na pasta Documentos)
4. A pasta `conselho-executivo-ia-main` é o seu conselho

**Opção B — Via terminal (se já tem Git):**

```bash
git clone https://github.com/luanalabrego/conselho-executivo-ia.git
```

### Passo 2 — Criar conta na Anthropic e pegar a API Key

1. Acesse **https://console.anthropic.com**
2. Crie uma conta (precisa de cartão de crédito — o custo é por uso, não assinatura)
3. Vá em **API Keys** → **Create Key**
4. Copie a chave (começa com `sk-ant-...`)
5. Guarde em lugar seguro — você vai usar no próximo passo

**Custo típico:** Uma sessão de conselho custa entre US$ 0,50 e US$ 2,00. Uso normal fica em torno de US$ 20/mês.

### Passo 3 — Instalar o Claude Code

Abra o terminal do seu computador e rode:

**No Mac/Linux:**
```bash
npm install -g @anthropic-ai/claude-code
```

**No Windows:**
```bash
npm install -g @anthropic-ai/claude-code
```

> Se não tem o Node.js instalado, baixe em https://nodejs.org (versão LTS).

### Passo 4 — Configurar a API Key

No terminal, rode:

```bash
claude config set apiKey sk-ant-SUA-CHAVE-AQUI
```

Substitua `sk-ant-SUA-CHAVE-AQUI` pela chave que você copiou no Passo 2.

### Passo 5 — Abrir o Conselho

No terminal, navegue até a pasta que você baixou:

```bash
cd ~/Documents/conselho-executivo-ia-main
```

> Ajuste o caminho conforme onde você salvou a pasta.

E inicie o Claude Code:

```bash
claude
```

### Passo 6 — Onboarding (primeira vez)

Na primeira vez, configure sua empresa digitando:

```
/council:conselho
```

E depois:

```
*onboarding
```

Responda 6 perguntas sobre sua empresa. Depois disso, todos os conselheiros conhecem seu negócio.

---

## Como Usar

### Reunião do Conselho (todos os C-levels debatem)

```
/council:conselho
*reuniao Definir estratégia de pricing para o próximo trimestre
```

### Debate sobre um tema específico

```
/council:conselho
*debate Vale a pena investir R$ 10K em tráfego pago agora?
```

### Conversar com um conselheiro específico

```
/council:cfo
Helena, preciso analisar se tenho caixa para contratar 2 pessoas
```

### Briefing Executivo (resumo de todos os dados)

```
/council:conselho
*briefing
```

### Ver decisões e ações pendentes

```
/council:conselho
*status
```

---

## Exemplos Práticos

| Situação | O que fazer |
|----------|-------------|
| "Quero definir o preço do meu produto" | `/council:conselho` → `*reuniao Definir pricing` |
| "Preciso decidir se contrato mais gente" | `/council:cfo` → pergunte sobre o caixa, depois `/council:coo` → pergunte sobre capacidade |
| "Quero montar estratégia de marketing" | `/council:cmo` → peça uma estratégia |
| "Tenho problema de churn" | `/council:cco` → peça análise de retenção |
| "Devo abrir uma nova frente de negócio?" | `/council:conselho` → `*debate Nova frente de negócio X` |

---

## Alimentando Dados (quanto mais, melhor)

Coloque dados da sua empresa na pasta `data/empresa/`. Quanto mais dados, melhores as recomendações.

| Tipo de dado | Quem usa | Formato |
|-------------|----------|---------|
| DRE, fluxo de caixa | Helena (CFO) | .md, .csv, .txt |
| Métricas de marketing (CAC, LTV, funil) | Marina (CMO) | .md, .csv |
| Dados de clientes (NPS, churn, feedback) | Caio (CCO) | .md, .txt |
| Pipeline de vendas, forecast | Rodrigo (CRO) | .md, .csv |
| Métricas operacionais, SLAs | Rafael (COO) | .md, .txt |
| OKRs, metas, roadmap | Victor (CEO) | .md |

Basta salvar os arquivos dentro de `data/empresa/` — os conselheiros leem automaticamente.

---

## Os 5 Princípios do Conselho

1. **Decisão Baseada em Dados** — Sem dados, sem decisão
2. **Debate Antes de Decidir** — Todo tema passa pelo conselho completo
3. **Transparência Total** — Tudo documentado, nada off the record
4. **Autoridade por Domínio** — Cada C-level manda no que é seu
5. **Voto de Minerva** — O CEO desempata, com justificativa

---

## Estrutura de Pastas

```
conselho-executivo-ia/
├── CLAUDE.md                    ← Cérebro do conselho (instruções da IA)
├── MANUAL.md                    ← Manual completo de uso
├── SETUP.md                     ← Guia de instalação detalhado
├── ONBOARDING.md                ← Configuração inicial
├── README.md                    ← Este arquivo
├── constitution.md              ← 5 princípios invioláveis
├── .claude/commands/council/    ← Comandos dos agentes
├── agents/                      ← Definições completas dos 7 agentes
├── templates/                   ← Templates de ata, decisão, briefing
└── data/
    ├── empresa/                 ← Dados da SUA empresa (alimente aqui)
    ├── decisoes/                ← Decisões salvas automaticamente
    ├── reunioes/                ← Atas salvas automaticamente
    └── memoria/                 ← Sistema de memória do conselho
```

---

## Preço

**Gratuito.**

O único custo é o uso da API da Anthropic (Claude). Uma sessão típica de conselho custa entre US$ 0,50 e US$ 2,00.

---

## Dúvidas Frequentes

**Preciso saber programar?**
Não. Basta seguir o passo a passo acima.

**Meus dados ficam seguros?**
Sim. Tudo roda localmente na sua máquina. Nenhum dado é enviado para servidores externos além da API da Anthropic (que não armazena suas conversas).

**Funciona em português?**
Sim, tudo em português.

**Posso personalizar os conselheiros?**
Sim, editando os arquivos em `agents/`.

**Quantas reuniões posso fazer?**
Ilimitadas. O limite é apenas o uso da API.

---

## Suporte

Dúvidas sobre instalação ou uso? Consulte o `MANUAL.md` dentro do pacote para instruções detalhadas.

---

*Conselho Executivo IA v1.0 — Seu conselho, suas decisões, seus dados.*
