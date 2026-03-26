# Setup — Conselho Executivo IA

Guia passo a passo para instalar e ativar seu Conselho Executivo com IA.

**Tempo estimado:** 10 minutos
**Requisitos:** Computador com internet

---

## Passo 1 — Instalar o Claude Code CLI

O Conselho Executivo roda no **Claude Code**, a ferramenta de linha de comando da Anthropic.

### No Mac (Terminal)

Abra o Terminal e cole:

```bash
npm install -g @anthropic-ai/claude-code
```

Se nao tiver o npm instalado, instale o Node.js primeiro:
- Acesse https://nodejs.org
- Baixe a versao LTS (recomendada)
- Instale normalmente
- Depois rode o comando acima

### No Windows (PowerShell)

Abra o PowerShell como administrador e cole:

```powershell
npm install -g @anthropic-ai/claude-code
```

### No Linux (Terminal)

```bash
npm install -g @anthropic-ai/claude-code
```

### Verificar Instalacao

Depois de instalar, verifique se funcionou:

```bash
claude --version
```

Deve mostrar a versao do Claude Code.

---

## Passo 2 — Configurar sua Chave da API Anthropic

Voce precisa de uma chave da API da Anthropic para usar o Claude.

### Criar a Chave

1. Acesse https://console.anthropic.com
2. Crie uma conta (se nao tiver)
3. Va em **API Keys**
4. Clique em **Create Key**
5. Copie a chave (comeca com `sk-ant-...`)

### Configurar a Chave

No terminal, rode:

```bash
claude config set apiKey sk-ant-SUA-CHAVE-AQUI
```

Ou defina como variavel de ambiente:

```bash
export ANTHROPIC_API_KEY=sk-ant-SUA-CHAVE-AQUI
```

Para deixar permanente no Mac/Linux, adicione ao `~/.zshrc` ou `~/.bashrc`:

```bash
echo 'export ANTHROPIC_API_KEY=sk-ant-SUA-CHAVE-AQUI' >> ~/.zshrc
source ~/.zshrc
```

### Quanto Custa?

A API da Anthropic cobra por uso. Uma sessao tipica do conselho (1 reuniao com debate completo) custa aproximadamente US$ 0.50 a US$ 2.00, dependendo da profundidade do debate.

---

## Passo 3 — Abrir o Conselho

### Navegar ate a Pasta

No terminal, va ate a pasta do conselho:

```bash
cd caminho/para/council-package
```

Por exemplo, se voce baixou na pasta Downloads:

```bash
cd ~/Downloads/council-package
```

### Iniciar o Claude Code

```bash
claude
```

O Claude Code vai abrir e carregar automaticamente o arquivo `CLAUDE.md` com todas as instrucoes do conselho.

---

## Passo 4 — Fazer o Onboarding (Primeira Vez)

Na primeira vez, configure sua empresa. Digite:

```
*onboarding
```

O conselho vai fazer 6 perguntas sobre sua empresa. Responda com detalhes — quanto mais contexto, melhores os conselhos.

Apos o onboarding, o perfil da sua empresa sera salvo e todos os conselheiros terao acesso ao contexto.

---

## Passo 5 — Sua Primeira Reuniao

Agora voce esta pronto. Teste com sua primeira reuniao:

```
*reuniao Definir prioridades para os proximos 30 dias
```

O conselho vai:
1. Consultar os dados da sua empresa
2. Cada C-level (CEO, CFO, COO, CMO, CCO, CRO) vai dar sua perspectiva
3. Levantar riscos e contrapontos
4. Sintetizar e propor uma decisao
5. Salvar a decisao automaticamente

---

## Comandos Rapidos

| Comando | O que faz |
|---------|-----------|
| `*reuniao {pauta}` | Reuniao completa do conselho |
| `*debate {tema}` | Debate entre C-levels sobre um tema |
| `*decisao {resumo}` | Registrar uma decisao |
| `*briefing` | Briefing executivo com dados da empresa |
| `*status` | Ver decisoes e acoes pendentes |
| `*help` | Listar todos os comandos |

## Ativar um Conselheiro Especifico

Use os slash commands para conversar com um conselheiro especifico:

| Comando | Conselheiro |
|---------|-------------|
| `/council/ceo` | Victor — Estrategia e visao |
| `/council/cfo` | Helena — Financas e investimentos |
| `/council/coo` | Rafael — Operacoes e processos |
| `/council/cmo` | Marina — Marketing e growth |
| `/council/cco` | Caio — Clientes e retencao |
| `/council/cro` | Rodrigo — Receita e vendas |
| `/council/conselho` | Conselho completo — Reunioes e debates |

---

## Alimentando Dados

Quanto mais dados voce colocar na pasta `data/empresa/`, melhores as recomendacoes.

Crie arquivos com os dados que voce tiver:

```
data/empresa/
├── perfil-empresa.md      (gerado no onboarding)
├── financeiro.md           (DRE, fluxo de caixa)
├── marketing.md            (CAC, LTV, campanhas)
├── clientes.md             (NPS, churn, feedback)
├── operacional.md          (metricas, SLAs)
└── vendas.md               (pipeline, forecast)
```

Formatos aceitos: `.md`, `.txt`, `.csv`, `.json`, `.yaml`

---

## Problemas Comuns

### "command not found: claude"
O Claude Code nao foi instalado. Rode `npm install -g @anthropic-ai/claude-code`.

### "API key not found"
A chave da API nao esta configurada. Rode `claude config set apiKey sk-ant-SUA-CHAVE`.

### "Permission denied"
No Mac/Linux, tente com `sudo`: `sudo npm install -g @anthropic-ai/claude-code`.

### O conselho nao conhece minha empresa
Execute `*onboarding` para configurar o perfil. Ou adicione dados em `data/empresa/`.

---

*Conselho Executivo IA — Setup v1.0*
