# Baralho Ética na Inteligência Artificial — v1.6.0 Render

## Arquitetura
- Node.js + Express
- SQLite nativo do Node (`node:sqlite`)
- 1 Web Service Render
- disco persistente montado em `/var/data`
- banco em `/var/data/baralho-etica.sqlite`

## Deploy no Render
1. Suba esta pasta para um repositório GitHub.
2. No Render, crie um **Blueprint** apontando para o repositório. O `render.yaml` cria o Web Service e o disco persistente.
3. Defina `ADMIN_PASSWORD` com uma senha forte.
4. Em `PUBLIC_BASE_URL`, informe a URL final, por exemplo `https://baralho-etica-ia.onrender.com`.
5. Faça o deploy.
6. Professor: `/professor`. Os links dos grupos aparecem no painel.

## SQLite no Render
Esta versão usa SQLite com disco persistente. Sem o disco, o filesystem do Render é efêmero e as participações seriam perdidas em reinícios/deploys. O Blueprint usa plano `starter` porque disco persistente não está disponível no plano Free.

## Resetar participações
O painel do professor possui **Resetar participações**. A ação exige duas confirmações e apaga:
- seleções atuais dos grupos;
- submissões dos encontros 1 e 2.

Ela **não altera** quais decks estão liberados/bloqueados e registra a ação no `audit_log`.

## Interface dos decks
Foi removido o botão redundante **Deixar todas viradas**. Permanece apenas **Revelar/fechar todas**.

## Pontuação
A matriz oculta da v1.5.4 foi preservada. O painel do professor continua exibindo valores das cartas, score por deck, score por encontro e score final após os dois encontros.
