# Usar com IA

Se a sua equipe usa IA para programar (Copilot, Claude, Cursor, Codex), dê a ela o padrão da plataforma. O
**`AGENTS.md`** é um arquivo de instruções que a IA lê antes de gerar código. Com ele, a tela já sai no Design
System MS, com login pelo SmartPass, um campo por linha e as regras de segurança.

**[Baixar o AGENTS.md](ia/agents.txt){ download="AGENTS.md" }** · [ver o arquivo](ia/agents.txt){ target=_blank }

## Como usar

1. Ponha o `AGENTS.md` na **raiz do repositório** do serviço que o Orquestrador criou.
2. Copilot, Cursor e Codex leem o arquivo sozinhos.
3. No **Claude Code**, crie também um `CLAUDE.md` na raiz com uma linha só:

    ```text
    @AGENTS.md
    ```

4. Peça o que precisa em linguagem normal. Exemplo:

    ```text
    Crie a tela de solicitação do serviço "Emitir certificado do ensino médio":
    o cidadão escolhe se é para ele ou para um dependente, confere os dados
    e envia um documento. Siga o AGENTS.md.
    ```

5. Antes de entregar, confira o [checklist](checklist.md) e peça a [homologação](homologacao.md).

!!! warning "A IA ajuda, mas não homologa"
    O código gerado passa pela revisão técnica da X-VIA e pela homologação com a SETDIG, como qualquer outro.

## Para a IA achar o guia

O site também tem um [`llms.txt`](llms.txt): um índice das páginas deste guia em formato que a IA lê. O Design
System MS tem o dele no pacote `@plataforma-xvia/ds-react`.

## O arquivo

O `AGENTS.md` só resume as regras e aponta para as páginas deste guia. Quando uma regra mudar aqui, ele muda junto.
