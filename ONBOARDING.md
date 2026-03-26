# Onboarding — Conselho Executivo IA

Este e o guia de configuracao inicial do seu Conselho Executivo. Execute este fluxo na primeira vez que usar o conselho.

---

## Como Executar

No Claude Code, digite:

```
*onboarding
```

Ou use o slash command:

```
/council/conselho
```

E depois digite `*onboarding`.

---

## Fluxo de Onboarding

O conselho vai guiar voce por 6 perguntas. Responda com o maximo de detalhes possivel — quanto mais contexto, melhores as recomendacoes dos conselheiros.

### Pergunta 1 — Sobre a Empresa

> **Qual o nome da sua empresa e o que ela faz?**
>
> Descreva seu produto ou servico principal. O que voce vende? Para quem?
>
> Exemplo: "A TechFlow e uma empresa de software que vende um CRM para pequenas empresas de servicos. Nosso diferencial e a simplicidade e integracao com WhatsApp."

### Pergunta 2 — Mercado e Clientes

> **Qual seu mercado-alvo?**
>
> B2B ou B2C? Quais segmentos? Quem e seu cliente ideal (ICP)?
>
> Exemplo: "B2B, focamos em empresas de servicos com 5-50 funcionarios. Nosso ICP e o dono da empresa que ainda usa planilha para gerenciar clientes."

### Pergunta 3 — Tamanho e Fase

> **Qual o tamanho da sua empresa hoje?**
>
> Numero de funcionarios, faixa de faturamento mensal, fase da empresa (pre-revenue, early stage, growth, scale).
>
> Exemplo: "Somos 8 pessoas, faturamento de R$ 80K/mes, estamos em fase de growth — produto validado, precisamos escalar."

### Pergunta 4 — Top 3 Desafios

> **Quais sao seus 3 maiores desafios agora?**
>
> Seja especifico. Nao precisa ser so negocios — pode ser time, produto, vendas, marketing, financeiro, operacional.
>
> Exemplo:
> 1. "Churn alto — 8% mensal, clientes saem depois de 3 meses"
> 2. "Nao consigo escalar vendas — dependo 100% de indicacao"
> 3. "Fluxo de caixa apertado — todo mes e um sufoco"

### Pergunta 5 — Decisoes Pendentes

> **Quais decisoes voce precisa tomar nos proximos 30 dias?**
>
> O que esta te tirando o sono? O que voce vem adiando?
>
> Exemplo:
> - "Contratar ou nao um vendedor dedicado"
> - "Aumentar o preco do plano basico"
> - "Investir em trafego pago ou focar em conteudo organico"

### Pergunta 6 — Dados Disponiveis

> **Que dados voce tem disponivel sobre sua empresa?**
>
> DRE, fluxo de caixa, metricas de marketing (CAC, LTV), NPS, pipeline de vendas, etc.
> Voce pode adicionar esses arquivos depois em `data/empresa/`.
>
> Exemplo: "Tenho uma planilha com DRE dos ultimos 6 meses e um dashboard no RD Station com metricas de marketing."

---

## O Que Acontece Depois

Apos responder as 6 perguntas, o conselho:

1. **Salva o perfil** em `data/empresa/perfil-empresa.md` com todos os dados fornecidos
2. **Registra na memoria institucional** em `data/memoria/institutional.md` os principios e contexto base
3. **Apresenta um briefing inicial** com as primeiras impressoes de cada C-level
4. **Sugere a primeira pauta** para reuniao do conselho baseada nos desafios apresentados

---

## Formato do Perfil Gerado

Apos o onboarding, o arquivo `data/empresa/perfil-empresa.md` tera este formato:

```markdown
# Perfil da Empresa — {Nome da Empresa}

> Gerado em {data} durante onboarding do Conselho Executivo IA

## Dados Basicos

- **Nome da empresa:** {resposta}
- **O que faz:** {resposta}
- **Produto/Servico principal:** {resposta}
- **Diferencial:** {resposta}

## Mercado e Clientes

- **Tipo:** B2B / B2C / B2B2C
- **Segmentos-alvo:** {resposta}
- **ICP (Cliente Ideal):** {resposta}
- **Tamanho do mercado:** {estimativa se mencionado}

## Tamanho e Fase

- **Funcionarios:** {numero}
- **Faixa de faturamento:** {range}
- **Fase:** {pre-revenue / early / growth / scale}
- **Modelo de receita:** {recorrente / transacional / misto}

## Desafios Atuais (Top 3)

1. {desafio 1 — detalhado}
2. {desafio 2 — detalhado}
3. {desafio 3 — detalhado}

## Decisoes Pendentes

- {decisao 1}
- {decisao 2}
- {decisao 3}

## Dados Disponiveis

{lista do que o usuario tem de dados / metricas}

## Notas Adicionais

{qualquer contexto extra relevante}
```

---

## Dica: Adicionando Dados Depois

Quanto mais dados voce colocar em `data/empresa/`, melhores as recomendacoes do conselho.

Crie arquivos separados para cada area:
- `data/empresa/financeiro.md` — DRE, fluxo de caixa, projecoes
- `data/empresa/marketing.md` — CAC, LTV, campanhas, funil
- `data/empresa/clientes.md` — NPS, churn, feedback
- `data/empresa/operacional.md` — metricas de time, SLAs
- `data/empresa/vendas.md` — pipeline, forecast, win rate

Formatos aceitos: `.md`, `.txt`, `.csv`, `.json`, `.yaml`

---

*Conselho Executivo IA — Onboarding v1.0*
