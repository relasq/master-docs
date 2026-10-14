# Master Developers

Documentação Mintlify da API pública da Master. Domínio de publicação: **https://docs.pagmaster.site**.

```sh
npm ci
npm run dev
```

Preview local: `http://localhost:3001`. `docs.json` organiza os guias e importa `openapi.yaml` como referência. A base de produção é `https://api.pagmaster.site/api/v1/public`.

Conecte este repositório ao projeto Mintlify e configure `docs.pagmaster.site` como domínio personalizado no serviço, com o DNS indicado por ele. Enviar o código ao GitHub não configura o domínio ou a hospedagem.

## Contrato

As rotas públicas incluem conta e pagamentos BRL, cobranças Pix e cartão, links de pagamento, saques automáticos e cripto com saldo USDT separado. Há uma única operação principal; subcontas são criadas pela API e selecionadas por `X-Master-Subaccount`. Sem o header, usa a principal. As keys são geradas em `https://www.pagmaster.site/dashboard/integrations/keys`.

`crypto.mdx` e os seis endpoints `/crypto/*` do OpenAPI descrevem unidades, taxa de 3%, polling, redes, saldo, reservas e repetição segura. Valores USDT são inteiros em milionésimos, não centavos BRL. Saques cripto usam TRC-20.

O OpenAPI documenta somente rotas de integração com bearer key. Rotas de sessão, administração e configuração do painel são internas à aplicação e estão descritas no repositório da API.
