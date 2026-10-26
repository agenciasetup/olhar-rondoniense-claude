---
name: noticia-de-release
description: Transforma release, link, PDF ou texto em notícia do Olhar Rondoniense, com chapéu, título, linha fina, texto, editoria, cidade e fonte, e salva como rascunho. Só publica quando pedirem.
---

# Notícia a partir de release

Versão 0.6, 22/10/2026. Salva no portal pelo conector "Olhar Rondoniense" (ferramentas abaixo). Aceita pauta da fila do portal pelo número (`pauta_id`).

Antes de escrever, leia `references/portal.md` (campos, limites, editorias, cidades e as regras que valem para todas as skills).

## Quando usar

O Gabriel manda um release de prefeitura, governo ou órgão público, um link de notícia, um PDF, um texto colado, um recado ("saiu a escala de vacinação em Ji-Paraná") ou uma pauta da fila do portal ("escreva a partir da pauta 123", o pedido que o botão "Pedir ao Claude" do painel copia) e quer a notícia pronta para o portal.

Se for vaga, concurso, seletivo ou estágio, use a skill `vaga-concurso`.

## Passo a passo

1. **Leia a origem inteira.** Link: abra. PDF: leia todo. Pauta da fila: abra o link do release (o resumo da fila é curto demais para escrever). Se não conseguir abrir, diga e peça o texto.
2. **Descubra o essencial:** o que aconteceu, onde (cidade), quando, quem, e por que importa para quem mora em Rondônia.
3. **Escolha a editoria e as cidades** pelas listas do portal (`listar_editorias`, `listar_cidades`); sem conector, pelas de `references/portal.md`.
4. **Escreva os campos** (abaixo).
5. **Confira** pelo checklist.
6. **Salve como rascunho** no portal (seção "Salvar no portal"). Sem conector, entregue os campos no chat, prontos para copiar.
7. **Responda** no formato do fim desta página.

## Como escrever

- **Primeiro parágrafo:** o fato principal, com quem, o quê, onde e quando. O leitor que parar ali já sabe o que aconteceu.
- **Depois:** detalhes em ordem de importância, frases curtas, um assunto por parágrafo.
- **Serviço em destaque:** data, horário, endereço, documentos, telefone e link vão perto do começo do texto, em frases normais (não precisa repetir em lista). Quando houver serviço, preencha também o **quadro de serviço**, que aparece em destaque na página: quando (dia e horário), onde (locais com endereço), como (quem pode e como fazer), documentos, contato e link (página oficial com mais informações; a página inicial do órgão não serve).
- **Em poucas palavras:** até 4 pontos, uma frase cada, com o essencial. Só o que está no texto, sem opinião, sem repetir o título nem a linha fina. Em notícia curta (até 4 parágrafos), ou quando o quadro de serviço já resume tudo, fica sem: na resposta, escreva "Em poucas palavras: sem (notícia curta)".
- **Intertítulos** (`<h2>`) só em texto longo, a cada quatro ou cinco parágrafos.
- **Sem propaganda:** "histórico", "grande conquista", "importante avanço" só entre aspas, na boca de alguém. Fala que só elogia, sem fato novo, vai curta no fim do texto ou sai; diga nas dúvidas o que fez com ela.
- **Declarações:** entre aspas, com nome e cargo de quem falou, como estão na origem.
- **Datas:** "nesta terça-feira (21)", "na próxima segunda-feira (27)". Horário de Rondônia. Confira se o dia da semana bate com a data; se a origem se contradiz ("sábado (25)" num mês em que o 25 é domingo), escreva como veio e ponha a dúvida em primeiro lugar.
- **Fonte:** o nome do órgão que divulgou ("Prefeitura de Rolim de Moura", não "Secom") e o link da página do release. Se só houver a página inicial, use e avise nas dúvidas.

### Release oficial ou notícia de outro veículo

| Origem | Pode | Não pode |
| --- | --- | --- |
| Release de órgão público ou de quem enviou para a redação | Aproveitar as informações e as falas, reorganizando em linguagem de notícia | Manter tom de propaganda; inventar o que não está lá |
| Notícia de jornal, site, rádio ou TV | Contar o fato com as nossas palavras, um trecho curto entre aspas, crédito com link ("As informações são do ...") | Copiar parágrafos; usar a foto deles |

Se a informação é exclusiva de outro veículo, avise o Gabriel e sugira confirmar com a fonte antes de publicar.

## Checklist antes de entregar

- [ ] Chapéu com até 20 caracteres.
- [ ] Título com até 300 caracteres e o essencial nas primeiras 70 letras.
- [ ] Linha fina com até 800 caracteres, sem repetir o título.
- [ ] "Em poucas palavras" com até 4 pontos, todos tirados do texto.
- [ ] Quadro de serviço preenchido quando há data, local ou passo a passo para o leitor.
- [ ] Editoria e cidades da lista.
- [ ] Fonte com nome e link.
- [ ] Nenhum número, nome, cargo, data ou fala que não esteja na origem.
- [ ] Foto oficial com crédito, ou "Foto: falta" (pedir à assessoria uma foto oficial com crédito).
- [ ] Dia da semana confere com a data.
- [ ] Nada copiado de outro veículo.

## Salvar no portal

Com o conector "Olhar Rondoniense" ligado:

1. `listar_editorias` e `listar_cidades`: use os nomes exatos.
2. `procurar_noticias` com duas ou três palavras do assunto (ela tenta todas as palavras e, sem resultado, qualquer uma). Se o portal já tem notícia do mesmo fato (mesma semana), não crie outra: avise o Gabriel, mande o link e pergunte se é para atualizar a que existe.
3. Foto oficial com link direto da imagem: `enviar_foto` (url, alt, credito). Sem foto, só com a página da foto, ou sem crédito: não suba e escreva "Foto: falta" na resposta. Se o release tiver várias fotos oficiais boas (evento, obra, mutirão), suba até 10 com `enviar_foto` e mande-as em `galeria`, na ordem em que contam a história; a melhor vai em `foto`.
4. `criar_rascunho` com todos os campos: chapeu, titulo, linha_fina, resumo, corpo_html, editoria, cidades, fonte_nome, fonte_url, foto (o objeto que `enviar_foto` devolveu) e servico, quando houver. Se a notícia veio de uma pauta da fila, mande também `pauta_id`: a pauta sai da fila do painel e fica ligada à notícia. Se a resposta disser que a pauta já virou notícia, não crie outra: mande o link da que existe e pergunte ao Gabriel o que fazer.
5. Leia `impedem_publicar` e `avisos` na resposta. O que dá para resolver com a origem, corrija com `editar_rascunho` (mande a `versao` que veio). O resto vira dúvida no fim da resposta.
6. `enviar_para_revisao` só quando o Gabriel pedir ("manda pra revisão").

Se as ferramentas do portal não aparecerem, o conector está desligado: entregue os campos no chat, prontos para copiar, e avise "Conector do portal desligado: o rascunho não foi salvo".

Rascunho é o padrão. Se o Gabriel pedir para publicar ("publica", "pode subir"): confira com `ler_noticia` que nada está em `impedem_publicar`, diga em uma frase o que vai publicar (título e se é agora ou agendado) e espere o "sim". Então `publicar_noticia` (com `quando` para agendar). Se a chave dele não puder publicar, o portal avisa: diga que a publicação é no painel, pelo editor-chefe, e mande o link.

## Formato da resposta

```
Rascunho salvo: <link do painel>   (ou: "Pronto para copiar" enquanto não houver conector)

Chapéu: ...
Título: ...
Linha fina: ...
Em poucas palavras:
- ...
- ...
Quadro de serviço (se houver): Quando: ... | Onde: ... | Como: ... | Documentos: ... | Contato: ...
Editoria: ...
Cidades: ...
Fonte: <nome> (<link>)
Foto: <arquivo ou link> | Crédito: ...   (ou: Foto: falta)
Galeria: <quantas fotos> (ou: sem galeria)

Texto:
...

Dúvidas para conferir antes de publicar:
- ...
```

Se não houver dúvidas, escreva "Sem dúvidas." Nunca deixe a seção de fora.
