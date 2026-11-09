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

O projeto `miris-cakes` está conectado a este repositório na Vercel. Novos commits enviados à branch `main` disparam uma publicação automática em https://miris-cakes.vercel.app.

O arquivo `vercel.json` configura o projeto estático e a pasta de saída `dist`, sem comando de build. Pull requests podem gerar prévias de revisão conforme as configurações da Vercel.

## Limitações desta versão

Este projeto é um protótipo com persistência em `localStorage`: os dados ficam apenas no navegador e não são compartilhados entre clientes. A área de gestão é demonstrativa e não possui autenticação. Não há banco de dados, pagamento, envio automático ou confirmação de encomendas. O link de WhatsApp permite ao cliente enviar o resumo após configurar o número da confeitaria.

Para operação real, implementar autenticação administrativa e armazenamento no servidor antes de receber pedidos de clientes. Hospedar na Vercel não altera essas limitações.

As imagens demonstrativas são do Unsplash. As imagens e fontes desta versão são servidas pelo próprio projeto; novas fotos configuradas por ID ainda podem usar o Unsplash.

## Identidade visual

- Miri’s Cakes: rosa antigo `#c77587`, rosa-claro `#ffd3ce` e tons derivados para contraste.
- Bebas Neue nos títulos e Poppins nos textos. Fontes incluídas com suas licenças OFL em `dist/assets/fonts`.
- Os destaques manuscritos priorizam Daydream quando instalada no dispositivo; Sacramento é a alternativa provisória incluída. O arquivo web da Daydream ainda precisa ser fornecido para uso consistente em todos os dispositivos.
- O cabeçalho usa o nome em texto até a disponibilização do arquivo original da logo.

