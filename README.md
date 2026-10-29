# Para estar com Deus - Leitor

Leitor web (estilo Kindle) do livro **Para estar com Deus - conselhos de vida interior para um catolico**, de Francisco Faus. O livro ja esta disponivel gratuitamente no site do autor; este projeto so oferece uma forma mais facil de ler.

## O que o leitor faz

- Guarda a ultima posicao de leitura no navegador (localStorage) - para qualquer visitante, sem login
- Botoes A- / A+ para ajustar o tamanho da letra (preferencia tambem salva)
- Sumario com a introducao e os 34 capitulos
- Funciona bem no celular (mobile-first)

## Publicar no Cloudflare (Workers Static Assets)

Pre-requisito: Node.js instalado.

```sh
npx wrangler login     # so na primeira vez (abre o navegador para autorizar)
npx wrangler deploy    # publica o site
```

Depois do deploy, o leitor fica no ar em:
`https://para-estar-com-deus.<seu-subdominio>.workers.dev`

## Estrutura

- `public/index.html` - o leitor completo (arquivo unico, sem dependencias)
- `wrangler.toml` - configuracao do deploy
