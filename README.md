# Olhar Rondoniense no Claude

Plugin da redação do [Olhar Rondoniense](https://olharondoniense.com.br) para o app do Claude e o Claude Code. Traz, numa instalação só:

- o **conector do portal** (o Claude opera o painel com o seu cargo; entra com o login do painel);
- as **skills da redação**: notícia a partir de release, vagas e concursos, pauta do dia, arte da notícia, post nas redes (Instagram, Facebook e Threads, com aprovação do editor-chefe) e tarefas da redação (diga "configura as tarefas da redação" no Claude do computador e ele agenda a pauta do dia e as outras).

Versão 0.8.0. O passo a passo com botões de copiar está no painel: **olharondoniense.com.br/admin/claude**.

## App do Claude (computador, site ou celular; planos Pro e Max)

Os nomes dos menus aparecem em português ou em inglês, conforme o idioma do seu Claude.

1. Ligue a execução de código: **Configurações > Capacidades** (*Settings > Capabilities*) > **Execução de código e criação de arquivos** (*Code execution and file creation*).
2. **Personalizar > Plugins > Adicionar > Adicionar marketplace** (*Customize > Plugins > Add > Add marketplace*) e cole: `agenciasetup/olhar-rondoniense-claude`
3. Em **Descobrir** (*Discover*), escolha **Olhar Rondoniense** e toque em **Adicionar** (*Add*).
4. No plugin, aba **Conectores** (*Connectors*): **Conectar** (*Connect*) em `olhar-rondoniense`. Abre a tela do painel: entre com o seu e-mail e senha e toque em **Permitir**.

Fica na sua conta: em outro computador ou no celular, é só entrar no mesmo Claude. As versões novas chegam sozinhas (para buscar na hora: **Personalizar > Plugins**, no marketplace, **Procurar atualizações**, *Check for updates*).

## Claude Code

```bash
claude plugin marketplace add agenciasetup/olhar-rondoniense-claude
claude plugin install olhar-rondoniense@olhar-rondoniense
```

Depois, no Claude Code, digite `/mcp`, escolha `olhar-rondoniense` e entre com o login do painel. Para atualizar: `claude plugin update olhar-rondoniense@olhar-rondoniense` (ou ligue a atualização automática em `/plugin` > Marketplaces).

## Para quem mantém

Este repositório é gerado a partir do repositório do portal (privado), pela pasta `redacao/`, com `scripts/publicar-plugin.sh`. Não edite aqui: a próxima publicação apaga.
