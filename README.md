# GMDB Saúde: frontend

## O que é

O GMDB Saúde ajuda municípios a acompanhar a vacinação contra o HPV e a detecção precoce do câncer do colo do útero. Ele mostra indicadores, lista pacientes por unidade e por ACS, e organiza campanhas e agendamentos de exames.

Os dados vêm do PEC do e-SUS APS de cada município.

O sistema tem três partes, cada uma num repositório:

- [gmdb-backend](https://github.com/RedFoxTech/gmdb-backend): API principal. NestJS, Prisma e PostgreSQL.
- [gmdb-frontend](https://github.com/RedFoxTech/gmdb-frontend): telas usadas pelas equipes de saúde. Next.js.
- [gmdb-pec-integration](https://github.com/RedFoxTech/gmdb-pec-integration): lê os dados do PEC de um município. Roda uma instância por município.

## Como rodar localmente

Requisitos: Node.js 22, Yarn e o [gmdb-backend](https://github.com/RedFoxTech/gmdb-backend) rodando.

```bash
cp .env.example .env.local   # aponte NEXT_PUBLIC_API_URL para o backend
yarn install
yarn dev -p 3002
```

Abra http://localhost:3002. A porta 3002 evita conflito com o backend e o PEC integration.

## Segurança

Para reportar uma falha, siga o [SECURITY.md](SECURITY.md). Não abra issue pública.

## Licença

[AGPL-3.0](LICENSE). Quem modificar o sistema e oferecer o uso dele pela rede precisa publicar as modificações com a mesma licença.
