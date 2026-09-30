# Master Developers

Documentação Mintlify da API pública da Master. Domínio de publicação: **https://docs2.loopbot.app**.

```sh
npm ci
npm run dev
```

Preview local: `http://localhost:3001`. `docs.json` organiza os guias e importa `openapi.yaml` como referência. A base de produção é `https://api2.loopbot.app/api/v1/public`.

Conecte este repositório ao projeto Mintlify e configure `docs2.loopbot.app` como domínio personalizado no serviço, com o DNS indicado por ele. Enviar o código ao GitHub não configura o domínio ou a hospedagem.

## Contrato

As rotas públicas incluem consulta de conta e pagamentos, cobranças Pix, preparação/confirmação/cancelamento de transferências e listagem/criação/renomeação/exclusão de operações de negócio. `X-Master-Operation` seleciona o negócio; sem ele, usa a principal atual. Sempre permanece pelo menos um negócio ativo. As keys são geradas no painel web, em `https://master.loopbot.app/dashboard/integrations/keys`.

O OpenAPI documenta somente rotas de integração com bearer key. Rotas de sessão, administração e configuração do painel são internas à aplicação e estão descritas no repositório da API.
