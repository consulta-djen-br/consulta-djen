# Indagatio

*Indagatio*, em latim, é a busca, a investigação. Site estático (sem servidor, sem banco de dados, sem cadastro).

- `index.html`: página inicial, com a apresentação e o botão para a consulta.
- `djen/index.html`: a ferramenta de busca de publicações na API pública de comunicações do CNJ
  (`https://comunicaapi.pje.jus.br/api/v1/comunicacao`). É um único arquivo; roda no navegador do usuário.
- `fonts/`: as três famílias do visual, em arquivos `.woff2`, cada uma com o texto da sua licença (SIL Open Font License 1.1):
  Besley (títulos), Atkinson Hyperlegible Next (texto) e Atkinson Hyperlegible Mono (números de processo, datas).
- `sitemap.xml`: lista as duas páginas para o Google (enviado pelo Search Console).
- `.nojekyll`: faz o GitHub Pages servir os arquivos como estão.

## Visual

A identidade vem do azulejo de São Luís: cobalto sobre louça, o número do processo numa placa de rua em cerâmica e o marca-texto rosa só no termo encontrado.
O motivo é próprio, inspirado na estrutura desses painéis (medalhão octogonal no centro de cada azulejo, estrela de oito pontas na junção dos quatro, rejunte entre eles) e desenhado em SVG: a parede da página inicial, a frisa do cabeçalho, o selo do logotipo e os medalhões numerados. Tudo usa as variáveis de cor, então acompanha os dois temas (`--vidrado` e `--rejunte` são o esmalte e o rejunte).

## Órgão e relator

No campo Órgão da busca, clicar abre a lista dos 26 órgãos de 2º grau do TJMA (câmaras, seções, Órgão Especial, Presidência), com o código que vai para a API; varas e juizados entram na lista depois que aparecem num resultado, e os últimos órgãos pesquisados ficam no topo. Nos resultados, o campo "Órgão ou relator" abre a lista do que existe na lista baixada, com a contagem de cada um; escolher um relator mostra um selo com o botão de tirar. A API não filtra por relator (ele é lido do texto), por isso os relatores só aparecem depois da busca.
Há dois temas, claro (Louça) e escuro (Noite), escolhidos pela preferência do sistema. Todo o CSS fica dentro de cada página, com as cores como variáveis (`--cobalto`, `--louca`, `--tinta` e as demais) no começo do bloco `<style>`.
Se as fontes não carregarem (por exemplo, ao abrir `djen/index.html` direto do computador ou rodá-lo pela página da API, o "plano B"), valem as fontes do sistema e tudo continua funcionando.

## Publicar e atualizar

O site é servido pelo GitHub Pages a partir da raiz da ramificação `main`. Cada envio para `main` atualiza o site em cerca de um minuto.
As preferências de cada pessoa ficam no navegador dela (localStorage), então uma atualização não apaga nada.

## Aparecer no Google

As duas páginas já vêm sem bloqueio de indexação, com descrição, endereço canônico e cartão de compartilhamento.
Para o Google descobrir o site mais rápido: no Search Console, adicione a propriedade por prefixo de URL
`https://consulta-djen-br.github.io/consulta-djen/`, confirme a posse (marcação HTML ou arquivo) e envie o `sitemap.xml`.
A indexação leva de alguns dias a algumas semanas. Não é possível usar `robots.txt` aqui, porque o site fica em um subcaminho de `github.io`.

## Observações

- A página só faz pedidos ao CNJ (a política de segurança do arquivo limita isso; as fontes só podem vir deste mesmo site). Nada do que é digitado é enviado a este site.
- Ferramenta independente e não oficial; não pertence ao CNJ nem a qualquer tribunal.
