# Modelo da arte da notícia

Versão 0.3, 26/10/2026. Linguagem inspirada no perfil de A Gazeta (ES), com a marca do Olhar. A arte é desenhada pelo próprio portal, sempre igual, a partir dos campos da notícia: aqui está o que cada peça leva, para conferir.

## Marca

| Elemento | Valor |
| --- | --- |
| Azul-marinho | `#002081` (faixa escura das artes: `#071437`) |
| Faixa da marca, da esquerda para a direita | `#0045CD` para `#058C7D` para `#2F9E4D` (12 px no pé de toda arte) |
| Amarelo de especial | `#FFCC29` (selo "Eleições 2026" e outras coberturas) |
| Selo | O ícone redondo (círculo verde e azul com o mapa de Rondônia), no canto de cima à direita |
| Títulos | Caladea Bold |
| Texto, etiquetas | Roboto; etiqueta do vídeo em Montserrat ExtraBold, maiúsculas |
| Cor da editoria | A mesma do site: Política azul, Polícia grafite, Cidades verde, Economia verde-água, Concursos azul-claro, Educação roxo, Saúde azul-céu, Entretenimento magenta |

## Peças

| Peça | Tamanho | Como é |
| --- | --- | --- |
| Post com foto | 1080 x 1350 | Foto em cima, ocupando o que sobra; embaixo, a faixa escura com chapéu (etiqueta branca, texto na cor da editoria), título grande e a linha fina. Um degradê liga a foto à faixa escura |
| Post sem foto | 1080 x 1350 | O degradê da editoria no fundo, com o círculo claro no canto (o mesmo da página da editoria no site); chapéu, título e linha fina embaixo |
| Carrossel | 1080 x 1350 | Capa = o post. Depois: "Em poucas palavras" (os pontos da notícia, numerados), "Inscrições" ou "Serviço" (o quadro de serviço) e a lâmina final com o endereço do site |
| Story | 1080 x 1920 | Como o post, deixando livres os 250 px de cima e de baixo (o Instagram cobre com o nome e a caixa de resposta) |
| Vídeo: camada do título | 1080 x 1920, fundo transparente | Para pôr nos primeiros 5 a 8 segundos do vídeo: etiqueta na cor da editoria, em maiúsculas, e o título em faixas brancas, letra escura. Cidade numa etiqueta escura em cima à esquerda; selo em cima à direita, que pode ficar o vídeo todo |
| Vídeo: cartela final | 1080 x 1920 | Fundo azul, o selo grande, o logo e o endereço do site. 1,5 segundo no fim do vídeo |

Cobertura especial (ex.: eleições): o selo vira a pílula amarela "Eleições 2026" com o ícone.

## Regras que o portal já cumpre

- Título inteiro, nunca cortado: quanto mais comprido, menor a letra. Acima de 150 caracteres fica pequeno demais: peça um título só para a arte (o da notícia não muda).
- Linha fina só quando o título tem até 120 caracteres; no máximo três linhas.
- Foto do Lenium com a faixa antiga da marca gravada em cima: a arte corta essa faixa sozinha.
- Crédito da foto no canto, quando a notícia tem crédito.

## O que conferir no olho (o portal não sabe)

- **Marca d'água antiga no meio da foto** (logo do Olhar e "olharondoniense.com.br" gravados na imagem, comum nas fotos de 2023 a 2025): não serve. Use o post sem foto ou outra foto.
- **Montagem de duas ou três fotos**: só serve se o rosto principal não ficar atrás do texto.
- **Rosto cortado ou atrás do título**: peça o recorte de cima (`foco: top`) ou de baixo (`foco: bottom`).

## Legenda do post (o jeito de A Gazeta, com a voz do Olhar)

```
<emoji do assunto> <o fato em uma frase, com o lugar e o dia>
⠀
<um ou dois parágrafos curtos com o que importa: números, quem, por quê>
⠀
⬛ <título de seção, quando houver serviço> ⬛
▪️ <prazo, onde, como, link>
⠀
🔗 Leia a notícia completa no link da bio.
⠀
#OlharRondoniense #<Cidade>
```

- A linha com "⠀" (um caractere em branco) mantém o espaço entre parágrafos no Instagram.
- Só fatos da notícia publicada, com as palavras dela; sem opinião e sem adjetivo de marketing.
- No máximo três hashtags.
- Sem travessão.
