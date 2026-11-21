# Indagatio

*Indagatio*, em latim, é a busca, a investigação. Site estático (sem servidor, sem banco de dados, sem cadastro).

- `index.html`: página inicial, com a apresentação e o botão para a consulta.
- `djen/index.html`: a ferramenta de busca de publicações na API pública de comunicações do CNJ
  (`https://comunicaapi.pje.jus.br/api/v1/comunicacao`). É um único arquivo; roda no navegador do usuário.
- `.nojekyll`: faz o GitHub Pages servir os arquivos como estão.

## Publicar e atualizar

O site é servido pelo GitHub Pages a partir da raiz da ramificação `main`. Cada envio para `main` atualiza o site em cerca de um minuto.
As preferências de cada pessoa ficam no navegador dela (localStorage), então uma atualização não apaga nada.

## Observações

- A página só faz pedidos ao CNJ (a política de segurança do arquivo limita isso). Nada do que é digitado é enviado a este site.
- Ferramenta independente e não oficial; não pertence ao CNJ nem a qualquer tribunal.
