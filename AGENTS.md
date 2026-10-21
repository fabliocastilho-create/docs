# Instruções do projeto de documentação

## Sobre este projeto

- Manual do Usuário do aplicativo **MSG POS AVEX** (versão de referência: 1.4.1), escrito em português brasileiro.
- Fonte da verdade: código-fonte do repositório `fabliocastilho-create/MPA_1.4.1` (frontend em `src/`, servidor em `backend/`).
- Páginas são arquivos MDX com frontmatter YAML. A navegação fica em `docs.json`.

## Limites de conteúdo

- Documente apenas funcionalidades implementadas e acessíveis ao usuário no código.
- Ignore completamente os módulos TASA e SAR. Não crie páginas, seções, campos ou exemplos sobre eles (inclusive a opção de abastecimento TASA e anexos CEPA TASA).
- Não inclua credenciais, dados pessoais, dados operacionais reais, endereços de servidor ou detalhes internos de implementação.
- Não descreva rotas da API nem nomes de variáveis como conteúdo para o usuário.
- Comportamentos que não puderem ser confirmados pelo código devem ficar marcados com o comentário `{/* CONFIRMAR: ... */}` em vez de serem afirmados.

## Terminologia

- Use os rótulos exatos da interface em negrito: **Iniciar Missão**, **Missões Anteriores**, **Mensagem de Posição**.
- "Mensagem de Posição" (abreviada "Msg Pos" apenas quando a interface usa a abreviação).
- Perfis: Gestor Global, Gestor CAvEx, Gestor Local, Administrador Local, Usuário.
- "Trigrama" para o identificador de login. "OMAvEx" para a organização militar.

## Estilo

- Segunda pessoa ("você"), voz ativa, frases curtas.
- Títulos em caixa de frase.
- Procedimentos sempre em `<Steps>` numerados.
- Regras e validações em tabelas; avisos em `<Warning>`, dicas em `<Tip>`, contexto de permissão em `<Info>`.
- Não use travessões (— ou –) como pontuação no texto novo.

## Capturas de tela

Não invente imagens. Reserve o espaço com o padrão abaixo, mantendo o identificador único no comentário para facilitar a substituição futura:

```mdx
{/* CAPTURA: identificador-unico */}
<Callout icon="camera" color="#6B7280">
  **Captura de tela pendente:** descrição do que a imagem deve mostrar.
</Callout>
```

Ao substituir, troque o bloco por `<Frame caption="...">![texto alternativo](/images/arquivo.png)</Frame>` e mantenha o comentário.
