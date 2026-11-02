# Como contribuir

Estas regras valem para pessoas e agentes de IA, em todos os repositórios da organização. Um repositório pode ter regras próprias, e elas prevalecem sobre estas.

## Fluxo

1. Todo trabalho relevante começa em uma issue, com critério de aceite e prioridade.
2. Crie uma branch a partir da `main`, no formato `tipo/numero-descricao`, como `fix/123-limite-upload`. O número é o da issue, quando houver. Use os mesmos tipos dos títulos de PR.
3. Rode `make verify` antes do push. A cota do Actions é limitada.
4. Abra o PR, juntando mudanças pequenas do mesmo assunto.
5. Faça squash merge com o CI verde. Enquanto a cota estiver esgotada, o merge exige `make verify` local e a menção disso no PR.

Nunca faça push na `main`. Ative a validação local uma vez em cada clone com `make hooks`. Essas regras não são impostas pelo servidor no plano atual, então dependem de todos as seguirem.

## CI

O CI roda em PR. A `main` é validada semanalmente ou manualmente antes de uma tag. Todo job precisa de `timeout-minutes`.

A cota é de 2.000 min/mês para a org inteira, e cada push num PR aberto roda o CI de novo. Por isso:

- Trabalhe com commits locais e dê um push só, quando a mudança estiver pronta e `make verify` passar. O hook `pre-push` (`make hooks`) roda `make verify` e recusa o push se falhar.
- Junte as correções pedidas na revisão num único push.
- O consumo do mês é acompanhado com `scripts/cota_actions.py`, que desliga workflows de menor prioridade antes de a cota acabar.

## Títulos de PR

Use Conventional Commits: `tipo(área): descrição`.

Tipos: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`, `ci`, `security`.

## Versões

Seguimos SemVer (`vMAJOR.MINOR.PATCH`). Cada milestone corresponde a uma versão, e produção recebe somente versões com tag. Só o dono do repositório cria tags e publica produção.

## Prioridades

- **P0:** bloqueia o uso ou envolve segurança. Resolver antes de novas funcionalidades.
- **P1:** importante, entra no próximo ciclo.
- **P2:** pode esperar.

## Decisões

Decisões de arquitetura ficam em ADRs, na pasta de decisões de cada repositório.

## Dados

Nunca inclua dados de clientes, dados pessoais ou credenciais em issues, PRs, commits ou logs.
