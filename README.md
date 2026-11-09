# Doce Ateliê

Aplicativo de encomendas para confeitaria, em português, com vitrine e pedidos temáticos.

## Recursos

A experiência prioriza o celular: navegação inferior fixa, resumo da sacola, catálogo em lista, filtros horizontais e formulários em tela cheia, com suporte à área segura do dispositivo.

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
- Logo original extraída do catálogo de Dia das Mães e aplicada como padrão, preservando logos personalizadas já salvas.


## Catálogos importados

Os PDFs originais ficam em `dist/assets/catalogs` e o cadastro inicial em `dist/assets/catalog-data.js`.

- Docinhos: 1 produto (100 unidades, até dois sabores dentre 13 opções). Preço de R$ 185,00 conforme o conteúdo do PDF; o nome do arquivo recebido indicava R$ 135,00.
- Sobremesas: 13 produtos, incluindo quatro sobremesas em três tamanhos, brownie com escolha de recheio, tortas, cheesecakes e tortas salgadas.
- Dia das Mães: 2 produtos, com opções de sabor, pães e bebida conforme cada cesta.
- Natal 2026 e Páscoa 2025: importação pendente. Os arquivos recebidos ultrapassaram o limite de transferência de 32 MiB; seus produtos e preços não foram lidos nem cadastrados. São exibidos apenas como pendências na gestão.

Os catálogos disponíveis começam ativos e podem ser ocultados na gestão. A atualização do cadastro remove os quatro produtos demonstrativos originais, adiciona os novos itens uma única vez e preserva pedidos e produtos personalizados já salvos. O WhatsApp do catálogo é usado quando não há um número personalizado configurado. Os preços de tamanhos e as opções de produtos podem ser editados na gestão.

As fotos de produtos foram extraídas dos PDFs fornecidos. Algumas imagens dos documentos eram capturas de tela de terceiros; nesses casos foi usada a logo como apresentação do produto, mantendo o PDF original disponível.
