---
name: arte-da-noticia
description: Faz as artes de uma notícia do Olhar Rondoniense para Instagram e Facebook (post, carrossel, story e a camada do título para vídeo), no modelo da marca, confere e entrega com a legenda do post.
---

# Arte da notícia

Versão 0.6, 27/10/2026. A arte é desenhada pelo próprio portal (linguagem inspirada em A Gazeta, com a marca do Olhar; ver `references/modelo.md`), para sair sempre igual e sem gastar IA. Esta skill pede a arte pelo conector (`fazer_arte`), confere pela prévia e entrega os links com a legenda. Você não desenha nem edita a imagem: se algo não ficou bom, peça de novo com outro ajuste.

Leia `references/portal.md` (regras gerais) e `references/modelo.md` (como a arte é).

## Quando usar

O Gabriel pede "faz a arte dessa notícia", "post para o Instagram", "carrossel", "story da manchete", "cartela do vídeo" ou manda o link de uma notícia do portal pedindo imagem.

## Passo a passo

1. **Ache a notícia** pelo link ou pelo número (`procurar_noticias` ou `ler_noticia`). Tem que estar publicada: arte de rascunho não sai.
2. **Peça ao portal** com `fazer_arte` as artes do pedido. Sem pedido específico: `post` e `story`. Carrossel (`post`, `resumo`, `servico`, `final`) quando a notícia tem "Em poucas palavras" ou quadro de serviço (a resposta diz: `tem_resumo`, `tem_servico`). Vídeo em pé: `reel` (camada do título, PNG transparente). Vídeo deitado (entrevista, imagem de TV): `moldura` (o título em cima, a marca embaixo e a janela transparente de 1080 x 608 no meio, onde entra o vídeo). Os dois com `fim` (cartela final).
3. **Confira cada prévia** pelo checklist. Se algo falhar, peça de novo com o ajuste: `foco` (rosto atrás do texto), `variante: "cor"` (foto com marca d'água antiga ou que não serve), `titulo_da_arte` (título longo demais), `especial: "eleicoes"` (cobertura das eleições). Nunca mude o título da notícia publicada por causa da arte.
4. **Escreva a legenda do post** no modelo de `references/modelo.md`: emoji do assunto e o fato na primeira linha, parágrafos curtos, serviço com ⬛ e ▪️ quando houver, "Leia a notícia completa no link da bio" e no máximo três hashtags (#OlharRondoniense e a cidade).
5. **Entregue** os links dos arquivos (o campo `arquivo` de cada arte) e a legenda. Vídeo: diga para pôr a camada do título nos primeiros 5 a 8 segundos (ou a moldura o vídeo todo, com o vídeo deitado encaixado na janela) e a cartela final no último segundo e meio.
6. **Para postar pelo portal** (Instagram, Facebook e Threads, com o editor-chefe aprovando no painel), siga a skill post-nas-redes: ela usa estas mesmas artes.

## Checklist da arte

- [ ] Título inteiro, sem corte e sem reticências (acima de 150 caracteres, sugira um título só para a arte).
- [ ] Nenhum texto em cima de rosto (senão, recorte `foco: top` ou `bottom`).
- [ ] Foto sem a marca d'água antiga no meio (senão, post sem foto ou outra foto).
- [ ] Crédito da foto visível, quando a notícia tem crédito.
- [ ] O nome "Olhar Rondoniense" e a pílula do site no pé (no story, só o nome).
- [ ] Chapéu na cor da editoria.
- [ ] Vaga e concurso: prazo de inscrição no carrossel (lâmina "Inscrições").

## Ferramentas

| Ferramenta | Para quê |
| --- | --- |
| `procurar_noticias`, `ler_noticia` | Achar a notícia e ver se está publicada |
| `fazer_arte` | Fazer as artes (formatos e ajustes acima); devolve os links e uma prévia de cada. A mesma arte pedida de novo sai na hora |

## Formato da resposta

```
Arte da notícia <número>: <título>
Post 4:5: <link do arquivo>
Story 9:16: <link do arquivo>
(e as outras que foram pedidas)

Legenda:
...

Conferido: título inteiro, crédito, faixa e logo. <ou o que falhou e a sugestão>
```
