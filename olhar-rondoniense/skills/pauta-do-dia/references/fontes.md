# Fontes oficiais de Rondônia

Conferidas em 21/10/2026 (só leitura).

**Fila do portal:** desde 22/10/2026 o portal lê sozinho, a cada 15 minutos, o feed destas fontes: Governo de Rondônia, Polícia Civil, Corpo de Bombeiros, IFRO, UNIR, prefeituras de Ji-Paraná, Vilhena, Rolim de Moura, Jaru, Guajará-Mirim e Buritis, Agência Brasil e Agência Senado. Com o conector, elas chegam por `listar_pautas`; as outras fontes desta lista continuam na pesquisa. O editor-chefe inclui fonte nova no painel (Pautas > Fontes).

 "RSS" é o endereço do feed, quando existe; ler o feed é mais rápido e mais confiável que abrir a página. Quando uma fonte não abrir, diga na resposta ("Fontes que não abriram") e siga com as outras.

**Período eleitoral:** em 21/10/2026 o portal do Governo de Rondônia (e as páginas de Sesau, Seduc, Detran, PM e demais secretarias, que moram nele) e o Diário Oficial do Estado estavam fechados ao público, com a comunicação de governo suspensa até o fim da eleição (25/10, se houver segundo turno). A Prefeitura de Porto Velho e o TJ-RO estavam em manutenção. Confira de novo depois de 25/10 e atualize esta lista.

## Estado

| Fonte | Página de notícias | RSS | Observação |
| --- | --- | --- | --- |
| Governo de Rondônia | https://rondonia.ro.gov.br/noticias/ | https://rondonia.ro.gov.br/feed/ | Fechado em 21/10 (período eleitoral). Secretarias em subpáginas: `/sesau/`, `/seduc/`, `/pm/`, `/pc/`, `/cbm/`, `/detran/`, `/sesdec/`, `/sedam/`, `/seas/` |
| Diário Oficial do Estado (DIOF) | https://diof.ro.gov.br/ | não tem | Fechado em 21/10. PDF do dia: `https://diof.ro.gov.br/data/uploads/AAAA/MM/DOE-DD-MM-AAAA.pdf` (e `-SUPLEMENTAR`). Concursos e nomeações |
| Sedam (meio ambiente) | https://www.sedam.ro.gov.br/noticias | não tem | Precisa de navegador (a lista só aparece com JavaScript) |
| Detran-RO | https://www.detran.ro.gov.br/noticias | não tem | Em 21/10 sem notícias; antes publicava no portal do Governo |

## Segurança

| Fonte | Página de notícias | RSS | Observação |
| --- | --- | --- | --- |
| Polícia Civil | https://www.pc.ro.gov.br/noticias/ | https://www.pc.ro.gov.br/feed/ | Ativa |
| Polícia Militar | https://www.pm.ro.gov.br/ | não verificado | Em manutenção em 21/10 |
| Corpo de Bombeiros | https://www.cbm.ro.gov.br/ | https://www.cbm.ro.gov.br/?feed=rss2 | |
| Defesa Civil | https://www.cbm.ro.gov.br/?cat=5 | https://www.cbm.ro.gov.br/?cat=5&feed=rss2 | Alertas de cheia, queimada, interdição |
| PRF | https://www.gov.br/prf/pt-br/noticias | não tem | Nacional, sem filtro por estado: procure "Rondônia", "BR-364", "BR-429", "BR-319" no título |

## Legislativo, contas e justiça

| Fonte | Página de notícias | RSS | Observação |
| --- | --- | --- | --- |
| Assembleia Legislativa (ALE-RO) | https://www.al.ro.leg.br/noticias/ | não tem | Ativa |
| Tribunal de Contas (TCE-RO) | https://tcero.tc.br/2026/10/ (troque o mês) | quebrado | Use o arquivo por mês |
| Ministério Público (MP-RO) | https://www.mpro.mp.br/pages/comunicacao/noticias | não tem | Lista pronta em https://www.mpro.mp.br/api/portal/noticias/grupos/publico?listGrupoId=3001&tipo=noticias&size=20&sort=dataExibicao,desc |
| Tribunal de Justiça (TJ-RO) | https://www.tjro.jus.br/ | não tem | Em manutenção em 21/10 |
| Defensoria Pública | https://www.defensoria.ro.def.br/noticias | não tem | Precisa de navegador |
| TRE-RO | https://www.tre-ro.jus.br/comunicacao/noticias | não tem | Precisa de navegador |
| MPF em Rondônia | https://www.mpf.mp.br/o-mpf/unidades/pr-ro/noticias | não tem | |
| Justiça Federal em RO | https://www.trf1.jus.br/sjro/imprensa/noticias | não tem | Publica pouco |

## Educação e concursos

| Fonte | Página | RSS | Observação |
| --- | --- | --- | --- |
| IFRO | https://portal.ifro.edu.br/ultimas-noticias | https://portal.ifro.edu.br/ultimas-noticias?format=feed&type=rss | Concursos e seleções: https://portal.ifro.edu.br/concursos-e-selecoes |
| UNIR | https://www.unir.br/noticia/lista | https://www.unir.br/feed | |
| Diário Oficial dos Municípios (AROM) | https://www.diariomunicipal.com.br/arom/ | não tem | Editais e seletivos das prefeituras. Busca em `/arom/pesquisar` |
| PCI Concursos (agregador, não é fonte oficial) | https://www.pciconcursos.com.br/concursos/norte/ | não tem | Só como pista: ache o edital oficial antes de virar pauta |
| SINE / Geração Emprego | https://geracaoemprego.ro.gov.br/ | não tem | Plataforma encerrada desde 01/09/2026; vagas do Sine saíam no portal do Governo |

## Porto Velho

| Fonte | Página de notícias | RSS | Observação |
| --- | --- | --- | --- |
| Prefeitura de Porto Velho | https://agencia.portovelho.ro.gov.br/noticias | não tem | Em manutenção em 21/10 |
| Câmara de Porto Velho | https://www.portovelho.ro.leg.br/noticias | não tem | |

## Interior (prioridade da pauta)

| Cidade | Página de notícias | RSS | Observação |
| --- | --- | --- | --- |
| Ji-Paraná | https://ji-parana.ro.gov.br/noticias/ | https://ji-parana.ro.gov.br/noticias/feed/ | Parada desde 22/09 |
| Ariquemes | https://ariquemes.ro.gov.br/blog | por secretaria: `/blog/<secretaria>/feed` | Não há feed geral |
| Vilhena | https://vilhena.ro.gov.br/imprensa/ | https://vilhena.ro.gov.br/feed/ | |
| Cacoal | https://cacoal.ro.gov.br/noticias.php | não tem | |
| Rolim de Moura | https://rolimdemoura.ro.gov.br/ | https://rolimdemoura.ro.gov.br/?feed=rss2 | Posts por secretaria |
| Jaru | https://jaru.ro.gov.br/category/noticias/ | https://jaru.ro.gov.br/feed/ | Feed com só 5 itens |
| Guajará-Mirim | https://guajaramirim.ro.gov.br/noticias/ | https://guajaramirim.ro.gov.br/feed/ | |
| Buritis | https://buritis.ro.gov.br/noticias/ | https://buritis.ro.gov.br/feed/ | |
| Espigão D'Oeste | https://espigaodooeste.ro.gov.br/noticias_site_categoria/1 | não tem | |
| Pimenta Bueno | https://pimentabueno.ro.gov.br/noticias/ | não tem | Sem data na lista: abra a notícia |
| Machadinho D'Oeste | https://machadinho.ro.gov.br/category/noticias/ | quebrado | |
| Ouro Preto do Oeste | https://ouropretodooeste.ro.gov.br/noticias | só editais | Quase parada |
| AROM (associação dos municípios) | https://arom.org.br/noticias | não tem | Assuntos de várias prefeituras |

Faltam as outras 39 prefeituras. Quando uma aparecer em pauta, confira o site e acrescente aqui.
