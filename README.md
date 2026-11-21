# Ferramentas de consulta

Site estático (sem servidor, sem banco de dados, sem cadastro).

- `index.html`: índice das ferramentas.
- `djen/index.html`: **Consulta DJEN**, busca de publicações na API pública de comunicações do CNJ
  (`https://comunicaapi.pje.jus.br/api/v1/comunicacao`). É um único arquivo; roda no navegador do usuário.
- `.nojekyll`: faz o GitHub Pages servir os arquivos como estão.

## Publicar

Qualquer hospedagem de arquivos estáticos serve (GitHub Pages, Netlify, Cloudflare Pages). A raiz do site é esta pasta.

## Atualizar

Troque `djen/index.html` pela versão nova e publique de novo. As preferências de cada pessoa ficam no navegador dela
(localStorage), então uma atualização não apaga nada.

## Observações

- A página só faz pedidos ao CNJ (a política de segurança do arquivo limita isso). Nenhum dado digitado é enviado a este site.
- Ferramenta independente e não oficial; não pertence ao CNJ nem a qualquer tribunal.
