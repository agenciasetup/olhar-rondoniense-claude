---
name: vaga-concurso
description: Lê edital de concurso, seletivo, estágio ou lista de vagas e monta a notícia do Olhar Rondoniense com o quadro de serviço (órgão, vagas, salário, prazo, link). Rascunho; só publica se pedirem.
---

# Vagas e concursos

Versão 0.5, 22/10/2026. Salva no portal pelo conector "Olhar Rondoniense" (ferramentas abaixo).

Antes de escrever, leia `references/portal.md` (campos, limites, editorias, cidades e regras gerais). O texto da notícia segue a skill `noticia-de-release`; aqui ficam só as regras próprias de vaga e concurso.

## Quando usar

O Gabriel manda um edital (PDF ou link), um aviso de seletivo, de estágio ou uma lista de vagas do SINE ou de empresa.

## O quadro de serviço

Aparece no portal antes do texto. Cada valor sai do edital, com a página de onde veio.

| Campo | Como preencher |
| --- | --- |
| Órgão | Nome oficial de quem contrata (ex. "Prefeitura de Cacoal"). Banca organizadora vai no texto |
| Vagas | Número total. Cadastro reserva escrito assim: "12 + cadastro reserva". Só cadastro: "cadastro reserva" |
| Salário | Valor exato. Faixa: "de R$ 1.518,00 a R$ 6.200,00". Com benefícios, só no texto |
| Prazo de inscrição | Data e hora do fim, no horário de Rondônia (converta se o edital usar Brasília) |
| Link do edital | O PDF oficial, no site do órgão ou da banca. Nunca site agregador |

Com o prazo preenchido, o portal mostra sozinho a contagem ("Faltam 3 dias", "Último dia") e o botão "Lembrar no calendário", e a vaga entra em /vagas-e-concursos pela data que vence primeiro. Por isso o prazo é o campo mais importante: confira duas vezes.

No texto, quando o edital trouxer: cargos e escolaridade, cidades das vagas, taxa de inscrição, data e local da prova, banca, isenção da taxa, como se inscrever.

## Regras próprias

1. **Edital é a única fonte de número.** Site agregador (PCI Concursos e parecidos) só serve de pista: ache o edital oficial e confira tudo nele.
2. **Retificação manda.** Se houver edital de retificação, use o mais recente e diga no texto o que mudou.
3. **Prazo vencido não vira notícia de inscrição.** Se o prazo já passou, avise o Gabriel antes de qualquer coisa.
4. **Inscrição ainda não aberta:** diga quando abre, além de quando fecha.
5. **Concurso, seletivo, estágio e vaga de emprego são coisas diferentes.** Use a palavra certa no chapéu: "Concurso", "Seletivo", "Estágio", "Vagas de emprego".
6. **Vagas para Rondônia em concurso nacional:** destaque quantas são aqui e em que cidades.
7. **Editoria:** Concursos. **Cidades:** as cidades das vagas.

## Passo a passo

1. Leia o edital inteiro (ou as seções de vagas, remuneração, inscrições, cronograma e taxa).
2. Preencha o quadro, anotando a página de cada valor.
3. Escreva o texto pela skill `noticia-de-release`, com o serviço no começo.
4. Confira o checklist.
5. Salve como rascunho (ou entregue no chat enquanto não houver conector).

## Checklist

- [ ] Os cinco campos do quadro preenchidos e com a página do edital.
- [ ] Prazo no horário de Rondônia e ainda aberto (ou aviso de vencido).
- [ ] Link do edital é o PDF oficial.
- [ ] Retificações conferidas.
- [ ] Chapéu certo (Concurso, Seletivo, Estágio ou Vagas de emprego).

## Salvar no portal

O mesmo caminho da `noticia-de-release` (listas, procurar, foto, `criar_rascunho`, conferir, corrigir), com:

- `editoria`: "concursos";
- `servico`: `{tipo: "vaga", orgao, vagas, salario, taxa, banca, edital_url}`, só com o que está no edital;
- `prazo_inscricao`: o último dia de inscrição, no formato AAAA-MM-DD, já no horário de Rondônia. É o que faz a contagem regressiva e o "Lembrar no calendário" funcionarem.

Antes de criar, `procurar_noticias` com o nome do órgão e "concurso" (ou "seletivo"). Edital que já tem notícia (retificação, prorrogação, resultado, convocação): avise o Gabriel e pergunte se é notícia nova ou atualização da que existe.

Rascunho é o padrão. Publicar só quando o Gabriel pedir, do mesmo jeito da `noticia-de-release` (conferir, dizer o que vai publicar, esperar o "sim", `publicar_noticia`).

## Formato da resposta

```
Rascunho salvo: <link do painel>   (ou: "Pronto para copiar")

QUADRO DE SERVIÇO
Órgão: ...                     (edital, p. X)
Vagas: ...                     (p. X)
Salário: ...                   (p. X)
Inscrições até: ...            (p. X)
Edital: <link do PDF oficial>

Chapéu / Título / Linha fina / Em poucas palavras / Editoria / Cidades / Fonte / Foto
(como na noticia-de-release)

Texto:
...

Dúvidas para conferir antes de publicar:
- ...
```
