# Manual do Usuario — Conselho Executivo IA

**Versao 1.0 | Labrego IA**

---

## Sumario

1. [Bem-vindo ao Conselho Executivo IA](#1-bem-vindo-ao-conselho-executivo-ia)
2. [Requisitos](#2-requisitos)
3. [Instalacao passo a passo](#3-instalacao-passo-a-passo)
4. [Primeiro uso — Onboarding](#4-primeiro-uso--onboarding)
5. [Conhecendo seus Conselheiros](#5-conhecendo-seus-conselheiros)
6. [Comandos disponiveis](#6-comandos-disponiveis)
7. [Exemplos praticos de uso](#7-exemplos-praticos-de-uso)
8. [Alimentando dados da sua empresa](#8-alimentando-dados-da-sua-empresa)
9. [Sistema de memoria](#9-sistema-de-memoria)
10. [Dicas para melhores resultados](#10-dicas-para-melhores-resultados)
11. [Perguntas frequentes (FAQ)](#11-perguntas-frequentes-faq)
12. [Suporte](#12-suporte)

---

## 1. Bem-vindo ao Conselho Executivo IA

### O que e

Imagine ter acesso a um conselho de administracao completo — com 6 executivos experientes, cada um especialista em uma area — disponivel 24 horas por dia, 7 dias por semana, pronto para debater qualquer decisao da sua empresa.

O **Conselho Executivo IA** e exatamente isso. E como ter um CEO, um diretor financeiro, um diretor de operacoes, um diretor de marketing, um diretor de clientes e um diretor de vendas sentados na mesa de reuniao, esperando voce trazer a pauta.

### Para que serve

- **Tomar decisoes estrategicas** com mais seguranca e fundamento
- **Analisar problemas** sob 6 perspectivas diferentes antes de decidir
- **Evitar pontos cegos** — cada conselheiro levanta riscos que voce talvez nao tenha visto
- **Documentar tudo** — todas as decisoes ficam registradas, com justificativa, votos e acoes
- **Ter um "segundo cerebro" estrategico** que conhece sua empresa e lembra das decisoes anteriores

### O que esperar

Pense no conselho como uma reuniao de diretoria. Voce traz um tema — "devo aumentar o preco?", "vale a pena contratar mais gente?", "como resolver o problema de clientes saindo?" — e cada conselheiro analisa o problema do ponto de vista da sua area.

Eles debatem entre si, levantam riscos, fazem contas quando tem dados, e no final o CEO do conselho sintetiza tudo e conduz a decisao. Tudo fica documentado automaticamente.

**Importante:** o conselho nao toma decisoes por voce. Ele te da a analise, os argumentos, os riscos e uma recomendacao fundamentada. A decisao final e sempre sua.

---

## 2. Requisitos

Para usar o Conselho Executivo IA, voce precisa de:

| Item | Detalhes |
|------|----------|
| **Computador** | Mac, Windows ou Linux — qualquer um serve |
| **Internet** | Conexao estavel (o conselho funciona online) |
| **Conta na Anthropic** | Gratuita para criar, mas o uso da IA tem custo (veja abaixo) |
| **Cartao de credito** | Para colocar creditos na Anthropic (~R$ 100/mes de uso tipico) |

### Sobre o custo

O Conselho Executivo IA em si e gratuito. O unico custo e o uso da IA da Anthropic (Claude), que funciona como uma conta de telefone pre-paga: voce coloca creditos e vai usando. Uma reuniao completa do conselho, com debate e decisao, custa tipicamente entre US$ 0,50 e US$ 2,00 (menos de R$ 12 por reuniao). Com US$ 20/mes (aproximadamente R$ 100), voce faz muitas reunioes e consultas.

---

## 3. Instalacao passo a passo

Nao se preocupe se voce nunca mexeu com isso antes. Vamos passo a passo, como montar um movel com manual de instrucoes. Sao 5 etapas e leva cerca de 10 minutos.

### Etapa 1 — Criar sua conta na Anthropic

A Anthropic e a empresa que faz a inteligencia artificial do conselho. Voce precisa de uma conta para usar.

1. Abra o navegador (Chrome, Safari, Edge — qualquer um)
2. Acesse: **https://console.anthropic.com**
3. Clique em **"Sign Up"** (Criar Conta)
4. Preencha com seu e-mail e crie uma senha
5. Confirme seu e-mail (vao te mandar um link)
6. Pronto — voce esta dentro do painel da Anthropic

### Etapa 2 — Colocar creditos

Ainda no painel da Anthropic:

1. No menu lateral, clique em **"Billing"** (Pagamento)
2. Adicione seu cartao de credito
3. Coloque pelo menos **US$ 10** de credito para comecar (recomendamos US$ 20)
4. Esse saldo vai sendo usado conforme voce faz reunioes e consultas

> **Dica:** e como carregar um celular pre-pago. Voce so paga pelo que usar.

### Etapa 3 — Gerar sua chave da API

A "chave da API" e como uma senha especial que permite o Conselho se conectar a inteligencia artificial. Pense nela como a chave de acesso ao seu escritorio virtual.

1. No painel da Anthropic (console.anthropic.com), va em **"API Keys"** no menu
2. Clique em **"Create Key"** (Criar Chave)
3. De um nome para a chave, por exemplo: "Conselho Executivo"
4. Clique em **"Create"**
5. **IMPORTANTE:** copie a chave que aparece (comeca com `sk-ant-...`). Guarde-a em local seguro — voce vai precisar dela daqui a pouco

> **Atencao:** essa chave so aparece UMA vez. Se perder, basta criar outra. E como uma senha — nao compartilhe com ninguem.

### Etapa 4 — Instalar o Node.js (se ainda nao tem)

O Node.js e um programa que precisa estar no computador para o Claude Code funcionar. E como instalar o Java para rodar um programa — voce instala uma vez e esquece.

1. Acesse: **https://nodejs.org**
2. Clique no botao verde que diz **"LTS"** (versao recomendada)
3. Baixe e instale normalmente (Proximo, Proximo, Concluir)
4. Reinicie o computador (recomendado)

Para verificar se instalou certo:
- No **Mac**: abra o Terminal (Aplicativos > Utilitarios > Terminal)
- No **Windows**: abra o PowerShell (clique direito no menu Iniciar > Windows PowerShell)
- Digite: `node --version` e aperte Enter
- Deve aparecer um numero como `v22.x.x` — isso significa que funcionou

### Etapa 5 — Instalar o Claude Code

Agora vamos instalar o programa do conselho. No mesmo Terminal (Mac) ou PowerShell (Windows), digite:

```
npm install -g @anthropic-ai/claude-code
```

Aperte Enter e espere. Vai aparecer um monte de texto na tela — e normal. Quando parar e aparecer o cursor piscando de novo, esta pronto.

Para confirmar que instalou certo, digite:

```
claude --version
```

Deve aparecer a versao do Claude Code. Se apareceu, parabens — esta tudo instalado!

### Etapa 6 — Abrir o Conselho pela primeira vez

Agora vamos abrir o conselho:

1. Descubra onde esta a pasta `council-package` no seu computador. Se voce descompactou o arquivo ZIP na area de trabalho, ela esta la.

2. No Terminal (Mac) ou PowerShell (Windows), navegue ate a pasta. Por exemplo:

   **No Mac:**
   ```
   cd ~/Desktop/council-package
   ```

   **No Windows:**
   ```
   cd C:\Users\SeuNome\Desktop\council-package
   ```

   > **Dica:** o comando `cd` significa "ir para a pasta" (change directory). Troque `SeuNome` pelo seu nome de usuario do Windows.

3. Agora digite:

   ```
   claude
   ```

4. Na primeira vez, ele vai pedir sua chave da API. Cole a chave que voce copiou na Etapa 3 (aquela que comeca com `sk-ant-...`).

5. O Claude Code vai abrir e carregar o conselho automaticamente. Voce vai ver uma tela de texto — e ali que tudo acontece.

**Pronto! O conselho esta instalado e funcionando.**

---

## 4. Primeiro uso — Onboarding

Na primeira vez que abrir o conselho, voce precisa apresentar sua empresa para os conselheiros. E como a primeira reuniao com um consultor novo — voce conta sobre o negocio para que ele possa te ajudar.

### Como iniciar

Com o Claude Code aberto (depois de seguir a Etapa 6 acima), digite:

```
*onboarding
```

E aperte Enter.

### As 6 perguntas

O conselho vai te fazer 6 perguntas. Responda com calma e com o maximo de detalhes que puder. Quanto mais voce contar, melhores serao os conselhos.

#### Pergunta 1 — Sobre a empresa

> "Qual o nome da sua empresa e o que ela faz?"

Conte o que voce vende, para quem, e qual e o diferencial.

**Exemplo de boa resposta:**
*"A TechFlow e uma empresa de software que vende um CRM para pequenas empresas de servicos. Nosso diferencial e a simplicidade — o dono da empresa consegue usar sem treinamento — e a integracao nativa com WhatsApp."*

#### Pergunta 2 — Mercado e clientes

> "Qual seu mercado-alvo?"

Voce vende para empresas (B2B) ou para consumidores finais (B2C)? Qual o perfil do seu cliente ideal?

**Exemplo de boa resposta:**
*"B2B, focamos em empresas de servicos com 5 a 50 funcionarios na regiao de Campinas-SP. Nosso cliente ideal e o dono da empresa que ainda usa planilha para gerenciar clientes e esta cansado de perder informacao."*

#### Pergunta 3 — Tamanho e fase

> "Qual o tamanho da sua empresa hoje?"

Quantas pessoas no time, quanto fatura por mes, em que momento esta.

**Exemplo de boa resposta:**
*"Somos 8 pessoas, faturamento de R$ 80 mil por mes, estamos em fase de crescimento — o produto ja esta validado e temos 120 clientes ativos. Agora o desafio e escalar."*

#### Pergunta 4 — Top 3 desafios

> "Quais sao seus 3 maiores desafios agora?"

Seja honesto e especifico. Pode ser qualquer area: vendas, financeiro, time, produto, marketing, operacao.

**Exemplo de boa resposta:**
*"1. Churn alto — 8% mensal, os clientes saem depois de 3 meses de uso. 2. Dependo 100% de indicacao para vender, nao tenho outro canal. 3. Fluxo de caixa apertado — todo mes e um sufoco para fechar as contas."*

#### Pergunta 5 — Decisoes pendentes

> "Quais decisoes voce precisa tomar nos proximos 30 dias?"

O que esta te tirando o sono? O que voce vem adiando?

**Exemplo de boa resposta:**
*"Preciso decidir se contrato um vendedor dedicado ou invisto esse dinheiro em trafego pago. Tambem preciso decidir se aumento o preco do plano basico de R$ 99 para R$ 149 — tenho medo de perder clientes."*

#### Pergunta 6 — Dados disponiveis

> "Que dados voce tem sobre a empresa?"

Planilhas, dashboards, relatorios — qualquer informacao que voce tenha. Voce pode adicionar esses arquivos depois.

**Exemplo de boa resposta:**
*"Tenho a DRE dos ultimos 6 meses numa planilha, um dashboard no RD Station com metricas de marketing, e o historico de NPS que fazemos por e-mail a cada trimestre."*

### O que acontece depois

Apos responder as 6 perguntas, o conselho:

1. **Salva o perfil da sua empresa** — todos os conselheiros passam a conhecer seu negocio
2. **Registra na memoria permanente** — o conselho nunca esquece essas informacoes
3. **Apresenta um briefing inicial** — cada conselheiro da sua primeira impressao
4. **Sugere a primeira pauta** — baseada nos desafios que voce mencionou

A partir daqui, voce esta pronto para usar o conselho. O onboarding so precisa ser feito uma vez.

---

## 5. Conhecendo seus Conselheiros

O conselho tem 6 executivos com personalidades e especialidades distintas, mais um orquestrador que coordena as reunioes. Pense neles como diretores de uma grande empresa — cada um olha para o mesmo problema de um angulo diferente.

### Victor — CEO (O Visionario)

**Papel:** Estrategia geral, visao de futuro, priorizacao e decisao final.

Victor e o lider do conselho. Ele pensa no longo prazo, enxerga o cenario completo e decide quando ha impasse entre os outros conselheiros. E como aquele socio experiente que ja viu muita coisa e sabe separar o urgente do importante.

**Quando usar:**
- Quando precisa priorizar — "tenho 5 coisas pra fazer e recurso pra 2"
- Quando precisa de visao estrategica — "para onde minha empresa deveria ir?"
- Quando outros conselheiros discordam e voce precisa de um desempate

**Exemplos de perguntas:**
- *"Victor, qual deveria ser a prioridade numero 1 da empresa nos proximos 90 dias?"*
- *"Victor, estou pensando em pivotar o modelo de negocio. Faz sentido?"*
- *"Victor, temos 3 oportunidades na mesa. Qual priorizar?"*

### Helena — CFO (A Guardia)

**Papel:** Financas, pricing, investimentos, orcamento e protecao do caixa.

Helena e a guardia do dinheiro. Ela analisa viabilidade financeira, projeta cenarios (otimista, realista, pessimista), calcula retorno sobre investimento e protege o caixa da empresa. E como ter uma diretora financeira que nao deixa voce gastar mais do que pode.

**Quando usar:**
- Quando envolve dinheiro — investir, contratar, aumentar preco, cortar custos
- Quando precisa de projecoes financeiras — "se fizer X, quanto gasto? Quando da retorno?"
- Quando precisa validar se o caixa aguenta uma decisao

**Exemplos de perguntas:**
- *"Helena, tenho caixa para contratar 2 pessoas agora?"*
- *"Helena, qual preco devo cobrar pelo meu servico?"*
- *"Helena, se eu investir R$ 10 mil em marketing, em quanto tempo tenho retorno?"*

### Rafael — COO (A Engrenagem)

**Papel:** Operacoes, processos, eficiencia, alocacao de time e SLAs.

Rafael e o cara dos processos. Ele mapeia gargalos, organiza fluxos de trabalho, define quem faz o que e garante que a operacao funcione sem travar. E como ter um gerente de operacoes que enxerga onde a empresa esta perdendo tempo e dinheiro.

**Quando usar:**
- Quando algo na operacao esta travando ou lento
- Quando precisa organizar processos — "como estruturar a entrega?"
- Quando precisa decidir sobre contratacao e alocacao de time

**Exemplos de perguntas:**
- *"Rafael, estamos demorando muito para entregar. Onde esta o gargalo?"*
- *"Rafael, como devo estruturar o time se contratar mais 3 pessoas?"*
- *"Rafael, qual processo devo automatizar primeiro?"*

### Marina — CMO (A Amplificadora)

**Papel:** Marketing, marca, aquisicao de clientes, growth e funil.

Marina cuida de tudo que envolve atrair clientes. Ela pensa em posicionamento de marca, canais de aquisicao, campanhas, funil de vendas e metricas como CAC (custo de aquisicao) e LTV (valor do cliente ao longo do tempo). E como ter uma diretora de marketing que sabe onde investir para trazer clientes.

**Quando usar:**
- Quando precisa atrair mais clientes — "como chego em mais gente?"
- Quando precisa posicionar a marca — "como quero ser visto pelo mercado?"
- Quando precisa decidir entre canais — "trafego pago ou conteudo organico?"

**Exemplos de perguntas:**
- *"Marina, qual a melhor estrategia de marketing para o meu tipo de negocio?"*
- *"Marina, devo investir em Instagram, LinkedIn ou Google Ads?"*
- *"Marina, como reduzo meu custo de aquisicao de clientes?"*

### Caio — CCO (A Ponte)

**Papel:** Clientes, retencao, experiencia do cliente, NPS e sucesso do cliente.

Caio e a voz do cliente dentro do conselho. Ele analisa por que clientes ficam, por que saem, o que reclamam e como melhorar a experiencia. E como ter um diretor de clientes que vive ouvindo o que o mercado fala da sua empresa.

**Quando usar:**
- Quando clientes estao saindo (churn) — "por que estao cancelando?"
- Quando precisa melhorar a experiencia — "como encantar o cliente?"
- Quando tem feedback negativo — "o que fazer com essas reclamacoes?"

**Exemplos de perguntas:**
- *"Caio, nosso churn esta em 8% ao mes. O que esta acontecendo?"*
- *"Caio, como estruturar um processo de sucesso do cliente?"*
- *"Caio, o NPS caiu de 60 para 40. Como reverter?"*

### Rodrigo — CRO (O Acelerador)

**Papel:** Receita, vendas, pipeline, go-to-market e maquina de vendas.

Rodrigo e o executivo de receita. Ele constroi a maquina de vendas — define processo comercial, metas, forecast, estrategia de go-to-market e parcerias. E como ter um diretor comercial que sabe transformar leads em clientes pagantes.

**Quando usar:**
- Quando precisa vender mais — "como acelero as vendas?"
- Quando precisa montar processo comercial — "como estruturar vendas?"
- Quando precisa de previsibilidade — "quanto vou faturar no proximo trimestre?"

**Exemplos de perguntas:**
- *"Rodrigo, como monto uma maquina de vendas previsivel?"*
- *"Rodrigo, devo contratar vendedores ou investir em self-service?"*
- *"Rodrigo, qual estrategia de go-to-market para o lancamento do novo produto?"*

### Conselho (O Orquestrador)

**Papel:** Coordenar reunioes e debates com todos os conselheiros ao mesmo tempo.

O Orquestrador nao e uma pessoa — e o "modo reuniao". Quando voce ativa o conselho completo, todos os 6 executivos participam juntos, debatem entre si e chegam a uma recomendacao coletiva.

**Quando usar:**
- Quando o tema e complexo e envolve varias areas
- Quando quer ouvir todos os pontos de vista antes de decidir
- Quando precisa de uma reuniao completa com debate

---

## 6. Comandos disponiveis

O conselho funciona com dois tipos de comandos: **slash commands** (para ativar conselheiros) e **comandos com asterisco** (para acoes do conselho).

### Ativar um conselheiro especifico

Use esses comandos quando quiser conversar com um conselheiro individual:

| Comando | Quem ativa | Para que |
|---------|-----------|---------|
| `/council/ceo` | Victor (CEO) | Estrategia, visao, priorizacao |
| `/council/cfo` | Helena (CFO) | Financas, pricing, investimentos |
| `/council/coo` | Rafael (COO) | Operacoes, processos, eficiencia |
| `/council/cmo` | Marina (CMO) | Marketing, growth, marca |
| `/council/cco` | Caio (CCO) | Clientes, retencao, experiencia |
| `/council/cro` | Rodrigo (CRO) | Vendas, receita, pipeline |
| `/council/conselho` | Conselho completo | Reunioes e debates com todos |

**Como usar:** digite o comando e depois sua pergunta. Por exemplo:

```
/council/cfo Helena, tenho caixa para contratar 2 pessoas?
```

### Comandos de acao

Use esses comandos para acoes especificas do conselho:

| Comando | O que faz | Quando usar |
|---------|-----------|-------------|
| `*reuniao {pauta}` | Inicia uma reuniao completa do conselho | Temas complexos que precisam de todos os conselheiros |
| `*debate {tema}` | Abre debate entre os C-levels | Quando quer ver diferentes opinioes sobre um tema |
| `*decisao {resumo}` | Registra uma decisao tomada | Apos uma reuniao, para formalizar o que foi decidido |
| `*briefing` | Gera um resumo executivo | Quando quer ver um panorama geral da empresa |
| `*status` | Mostra decisoes e acoes pendentes | Para acompanhar o que esta em andamento |
| `*help` | Mostra todos os comandos | Quando esquecer algum comando |

**Exemplos:**

```
*reuniao Definir prioridades para o proximo trimestre
```

```
*debate Vale a pena investir em trafego pago agora?
```

```
*briefing
```

> **Dica:** o comando `*reuniao` e o mais poderoso. Ele ativa todos os conselheiros, cada um analisa o tema, eles debatem e chegam a uma recomendacao documentada.

---

## 7. Exemplos praticos de uso

Aqui estao 5 situacoes reais do dia a dia de um empresario e como o conselho pode ajudar:

### Exemplo 1 — "Quero definir o preco do meu produto"

Definir preco envolve financas, marketing e vendas. Voce pode chamar os 3:

```
*reuniao Preciso definir o preco do meu novo servico de consultoria
```

**O que vai acontecer:**
- **Helena (CFO)** vai calcular o custo, margem minima e ponto de equilibrio
- **Marina (CMO)** vai analisar o posicionamento de marca e quanto o mercado aceita pagar
- **Rodrigo (CRO)** vai avaliar o impacto no processo de vendas e nas taxas de conversao
- **Os outros conselheiros** vao complementar com perspectivas de operacao e experiencia do cliente
- **Victor (CEO)** vai sintetizar e recomendar uma faixa de preco com justificativa

### Exemplo 2 — "Preciso decidir se contrato mais gente"

Contratacao afeta operacoes, financeiro e estrategia:

```
*reuniao Estou considerando contratar 3 pessoas. Faz sentido agora?
```

**O que vai acontecer:**
- **Rafael (COO)** vai mapear a necessidade operacional — onde esta o gargalo, que perfis precisa
- **Helena (CFO)** vai analisar se o caixa aguenta, calcular o impacto no fluxo e o payback
- **Victor (CEO)** vai avaliar se o timing e certo e se esta alinhado com a estrategia
- O conselho vai recomendar: contratar ou nao, quantas pessoas, quando e em que ordem

### Exemplo 3 — "Quero montar uma estrategia de marketing"

Se o tema e focado em marketing, voce pode conversar direto com a Marina:

```
/council/cmo Marina, preciso de uma estrategia de marketing para os proximos 3 meses. Hoje dependo so de indicacao e quero diversificar canais. Meu budget e R$ 5 mil por mes.
```

**O que vai acontecer:**
- Marina vai analisar os dados da sua empresa (se voce ja alimentou a pasta de dados)
- Vai recomendar canais, tipos de campanha e distribuicao de budget
- Vai definir metas e metricas para acompanhar

### Exemplo 4 — "Tenho um problema de churn"

Churn (clientes saindo) e uma pauta urgente que combina clientes e estrategia:

```
*debate Nosso churn subiu de 5% para 8% nos ultimos 2 meses. O que esta acontecendo e como resolver?
```

**O que vai acontecer:**
- **Caio (CCO)** vai analisar padroes de saida, feedback de clientes e possibilidades de causa
- **Victor (CEO)** vai avaliar o impacto estrategico e priorizar acoes
- **Os demais** vao complementar: Helena com o impacto financeiro, Rodrigo com a visao de vendas, Rafael com processos
- O conselho vai propor um plano de acao com prazos e responsaveis

### Exemplo 5 — "Quero debater se abro uma nova frente de negocio"

Abrir uma nova frente e uma decisao estrategica que merece reuniao completa:

```
*reuniao Estou pensando em lancar um produto novo para outro segmento de mercado. Temos capacidade? Vale a pena?
```

**O que vai acontecer:**
- **Victor (CEO)** vai avaliar o alinhamento estrategico e o risco de perder foco
- **Helena (CFO)** vai projetar o investimento necessario e o tempo ate o breakeven
- **Rafael (COO)** vai analisar se a operacao atual aguenta mais um produto
- **Marina (CMO)** vai avaliar o mercado e a estrategia de entrada
- **Rodrigo (CRO)** vai pensar no go-to-market e no modelo de vendas
- **Caio (CCO)** vai alertar sobre o impacto nos clientes atuais
- A decisao sera documentada com votos, riscos e plano de acao

---

## 8. Alimentando dados da sua empresa

O conselho funciona melhor quando tem dados reais sobre sua empresa. Pense assim: quanto mais informacao voce der, mais especifico e util sera o conselho. E como ir ao medico — se voce leva os exames, o diagnostico e muito mais preciso.

### Onde colocar os dados

Todos os dados ficam na pasta `data/empresa/` dentro da pasta do conselho. Voce pode criar arquivos de texto simples (`.md` ou `.txt`) com as informacoes.

### O que colocar

#### Financeiro (Helena agradece)
Crie um arquivo `data/empresa/financeiro.md` com:
- Faturamento mensal dos ultimos meses
- Custos fixos e variaveis
- Fluxo de caixa (quanto entra, quanto sai)
- Margem de lucro
- Projecoes (se tiver)

**Exemplo simples:**
```
# Financeiro — Minha Empresa

## Faturamento Mensal (2026)
- Janeiro: R$ 65.000
- Fevereiro: R$ 72.000
- Marco: R$ 68.000

## Custos Fixos: R$ 45.000/mes
- Folha: R$ 30.000
- Aluguel + infraestrutura: R$ 8.000
- Software e ferramentas: R$ 3.500
- Contabilidade: R$ 1.500
- Outros: R$ 2.000

## Margem liquida media: 18%
```

#### Clientes (Caio precisa)
Crie um arquivo `data/empresa/clientes.md` com:
- Numero de clientes ativos
- Taxa de churn (cancelamento) mensal
- NPS (se tiver)
- Principais reclamacoes ou elogios
- Ticket medio

#### Marketing (Marina usa)
Crie um arquivo `data/empresa/marketing.md` com:
- De onde vem seus clientes (indicacao, Google, redes sociais, etc.)
- Custo de aquisicao (CAC) — quanto gasta para conseguir um cliente
- Investimento em marketing mensal
- Metricas de funil (visitantes, leads, clientes)

#### Operacional (Rafael quer)
Crie um arquivo `data/empresa/operacional.md` com:
- Tamanho do time e funcoes
- Principais processos
- Gargalos conhecidos
- SLAs (tempo de resposta, entrega, etc.)

#### Vendas (Rodrigo vive disso)
Crie um arquivo `data/empresa/vendas.md` com:
- Pipeline de vendas (quantos deals em andamento)
- Taxa de conversao
- Ciclo medio de venda
- Ticket medio
- De onde vem os leads

### Formatos aceitos

Voce pode usar qualquer um destes formatos:
- `.md` (Markdown — texto simples com formatacao)
- `.txt` (texto puro)
- `.csv` (planilha exportada)
- `.json` (dados estruturados)
- `.yaml` (configuracoes)

> **Dica:** nao precisa ser perfeito. Mesmo um arquivo de texto simples com as informacoes ja ajuda muito. Voce pode ir adicionando e melhorando com o tempo.

---

## 9. Sistema de memoria

Uma das grandes vantagens do Conselho Executivo IA e que ele **lembra** das decisoes anteriores, do contexto da empresa e do historico de debates. E como um conselheiro de verdade que vai acumulando conhecimento sobre o seu negocio ao longo do tempo.

### Como funciona

O conselho tem 3 "gavetas" de memoria:

#### Memoria de curto prazo (sessao)
- Lembra do que voces conversaram na sessao atual
- Quando voce fecha e abre novamente, essa memoria e zerada
- Pense como um bloco de anotacoes da reuniao de hoje

#### Memoria de medio prazo (90 dias)
- Armazena acoes em andamento, tarefas pendentes e acompanhamentos
- Informacoes expiram apos 90 dias se nao forem atualizadas
- Pense como a sua lista de tarefas e follow-ups

#### Memoria permanente (institucional)
- Armazena decisoes formais, politicas e principios definidos
- Nunca expira — fica para sempre
- Pense como o livro de atas da sua empresa

### O que isso significa na pratica

- Se voce decidiu em janeiro que o preco do servico e R$ 199, o conselho vai lembrar disso em marco
- Se voce tem uma politica de 30 dias de teste gratis, todos os conselheiros sabem
- Se houve um debate sobre contratar vs. terceirizar, o historico esta la
- Decisoes passadas influenciam recomendacoes futuras — o conselho evolui com sua empresa

### Voce nao precisa fazer nada

A memoria e **automatica**. Os conselheiros salvam informacoes sozinhos, sem voce precisar pedir. Basta usar o conselho normalmente.

---

## 10. Dicas para melhores resultados

### Seja especifico nas perguntas

Em vez de perguntar *"como melhoro minha empresa?"*, pergunte *"como reduzo meu churn de 8% para 4% nos proximos 3 meses?"*. Quanto mais especifica a pergunta, mais util a resposta.

### Forneca dados concretos

Em vez de dizer *"estou vendendo pouco"*, diga *"fecho 3 clientes por mes, minha meta e 8, e o ticket medio e R$ 2.500"*. Numeros fazem toda a diferenca.

### Peca debate antes de decidir

Quando tiver um tema importante, use `*reuniao` ou `*debate` para ouvir todos os conselheiros. Cada um vai levantar riscos e oportunidades que voce talvez nao tenha pensado.

### Documente todas as decisoes

Use `*decisao` para registrar o que foi decidido. Isso cria um historico valioso e permite revisitar decisoes depois com `*revisar`.

### Alimente a pasta de dados regularmente

A cada mes, atualize os dados em `data/empresa/`. Quanto mais atualizados os dados, mais precisas as recomendacoes.

### Use *reuniao para temas complexos

Se o tema envolve multiplas areas (por exemplo, contratar + budget + estrategia), use `*reuniao` para ter a analise completa de todos os conselheiros.

### Comece simples

Nao tente usar tudo de uma vez. Comece com uma conversa simples com um conselheiro, depois faca uma reuniao, e va explorando aos poucos. O conselho se adapta ao seu ritmo.

---

## 11. Perguntas frequentes (FAQ)

### Quanto custa usar o Conselho Executivo IA?

O conselho em si e gratuito. O unico custo e o uso da API da Anthropic (a inteligencia artificial por tras). O custo tipico e de US$ 10 a US$ 20 por mes (aproximadamente R$ 50 a R$ 100), dependendo de quanto voce usar. Cada reuniao completa custa entre US$ 0,50 e US$ 2,00.

### Meus dados ficam seguros?

Sim. Todos os dados ficam **no seu computador**, na pasta do conselho. Nada e enviado para servidores externos, salvo em nuvem ou compartilhado com terceiros. As conversas com a IA sao processadas pela Anthropic com politicas rigorosas de privacidade, e seus dados nao sao usados para treinar a IA.

### Preciso saber programar?

Nao. Tudo funciona digitando comandos simples em texto. Se voce sabe digitar no WhatsApp, sabe usar o conselho. Os unicos momentos "tecnicos" sao a instalacao (que voce faz uma vez seguindo este manual) e navegar ate a pasta no terminal.

### Funciona em portugues?

Sim. O conselho foi inteiramente configurado para conversar em portugues. Todos os conselheiros falam portugues, as decisoes sao documentadas em portugues, e voce pode (e deve) escrever suas perguntas em portugues.

### Posso personalizar os conselheiros?

Sim. Os arquivos de cada conselheiro ficam na pasta `agents/`. Voce pode editar esses arquivos para ajustar a personalidade, o tom, ou adicionar contexto especifico. Mas isso e completamente opcional — os conselheiros ja vem configurados e prontos para uso.

### Quantas reunioes posso fazer?

Ilimitadas. Voce pode fazer quantas reunioes, debates e consultas quiser. O unico limite e o saldo de creditos na sua conta da Anthropic.

### O conselho substitui um consultor de verdade?

O conselho e uma ferramenta complementar. Ele e excelente para estruturar pensamento, analisar decisoes sob multiplas perspectivas e documentar tudo. Mas para questoes muito especificas (juridico, contabil, regulatorio), consulte sempre um profissional especializado.

### Posso usar em mais de uma empresa?

Sim. Basta ter uma pasta `council-package` separada para cada empresa, cada uma com seus proprios dados e onboarding. Cada pasta funciona de forma independente.

### O que acontece se eu fechar o terminal sem querer?

Nada se perde. As decisoes e dados da empresa continuam salvos nos arquivos. Basta abrir o terminal novamente, navegar ate a pasta e digitar `claude` para retomar.

### Funciona no celular?

No momento, o Conselho Executivo IA funciona apenas em computador (Mac, Windows ou Linux). Nao ha versao para celular.

---

## 12. Suporte

Se tiver qualquer duvida, problema na instalacao ou sugestao, entre em contato:

**Lucas — Labrego IA**

- **WhatsApp:** (11) 99110-8378
- **E-mail:** lucas@labrego.ai
- **LinkedIn:** linkedin.com/in/luanalabrego

Estamos a disposicao para ajudar voce a tirar o maximo do seu Conselho Executivo.

---

*Conselho Executivo IA v1.0 — Manual do Usuario*
*Labrego IA — Seu conselho, suas decisoes, seus dados.*
