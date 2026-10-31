# Como contribuir

Estas regras valem para pessoas e agentes de IA, em todos os repositórios da organização. Um repositório pode ter regras próprias, e elas prevalecem sobre estas.

## Fluxo

1. Todo trabalho relevante começa em uma issue, com critério de aceite e prioridade.
2. Crie uma branch curta a partir da `main`.
3. Rode a verificação local antes de enviar.
4. Abra o PR como rascunho e marque como pronto quando a verificação passar.
5. Faça squash merge somente com o CI verde. Falta de minutos de CI bloqueia o merge.

## Títulos de PR

Use Conventional Commits: `tipo(área): descrição`.

Tipos: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`, `ci`, `security`.

## Versões

Seguimos SemVer (`vMAJOR.MINOR.PATCH`). Cada milestone corresponde a uma versão, e produção recebe somente versões com tag.

## Prioridades

- **P0:** bloqueia o uso ou envolve segurança. Resolver antes de novas funcionalidades.
- **P1:** importante, entra no próximo ciclo.
- **P2:** pode esperar.

## Decisões

Decisões de arquitetura ficam em ADRs, na pasta de decisões de cada repositório.

## Dados

Nunca inclua dados de clientes, dados pessoais ou credenciais em issues, PRs, commits ou logs.
