# Doce Ateliê

Aplicativo de encomendas para confeitaria, em português, com vitrine e pedidos temáticos.

## Recursos

- Ativação e desativação de catálogos e produtos.
- Personalização de nome, cor, textos, produtos e preços.
- Montagem de bolo temático com tema, cor, tamanho, massa, recheio e mensagem.
- Sacola, solicitação de encomenda e resumo para WhatsApp.
- Gestão local de pedidos e seus status.

## Executar localmente

Não requer instalação nem etapa de build. Com Python 3:

```sh
python3 -m http.server 3000 --directory dist
```

Acesse http://localhost:3000.

## Publicar na Vercel

Importe este repositório em https://vercel.com/new. Use o diretório raiz do repositório. O arquivo `vercel.json` configura o projeto estático e a pasta de saída `dist`, sem comando de build. A integração GitHub da Vercel pode publicar automaticamente novos commits da branch principal.

## Limitações desta versão

Este projeto é um protótipo com persistência em `localStorage`: os dados ficam apenas no navegador e não são compartilhados entre clientes. A área de gestão é demonstrativa e não possui autenticação. Não há banco de dados, pagamento, envio automático ou confirmação de encomendas. O link de WhatsApp permite ao cliente enviar o resumo após configurar o número da confeitaria.

Para operação real, implementar autenticação administrativa e armazenamento no servidor antes de receber pedidos de clientes. Hospedar na Vercel não altera essas limitações.

As imagens usam Unsplash e as fontes usam Google Fonts, dependendo de conexão com esses serviços.
