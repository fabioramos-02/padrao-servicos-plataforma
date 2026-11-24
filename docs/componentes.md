# Componentes do formulário

**X-Forms e Orquestrador usam os mesmos componentes:** os da seção **Formulários** do
[Design System MS no Storybook](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-checkbox--docs).
A tela do cidadão no X-Forms (o Visualizar) já é montada com eles. No Orquestrador, a equipe usa os mesmos. Assim o
cidadão vê o mesmo formulário nas duas ferramentas.

## Qual componente usar

A fonte é o `@plataforma-xvia/ds-react` e o `llms.txt` dele.

| Campo | Componente | Observação |
|---|---|---|
| Texto curto, CPF, e-mail, telefone | [`ds-input`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-input--docs) | Rótulo em cima, **ajuda abaixo do campo**, que vira mensagem de erro |
| Texto longo com contador | [`ds-textarea`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-textarea--docs) | `maxlength` liga o contador "atual/máximo" |
| Data | `ds-input type="date"` | O próprio DS manda usar este, não o calendário |
| Opção única | [`ds-radio`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-radio--docs) | **Falta o grupo**: o `fieldset` com `legend` é da aplicação |
| Várias opções | [`ds-checkbox`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-checkbox--docs) | **Falta o grupo**, como no radio |
| Lista | [`ds-select`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-select--docs), [`ds-combobox`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-combobox--docs) | Lista longa ou com busca: `ds-combobox` |
| Arquivo | [`ds-file-drop`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-file-drop--docs) | Formato e tamanho na linha de ajuda |
| Código (SMS, e-mail) | [`ds-code-input`](https://designsystem.digital.ms.gov.br/?path=/docs/formul%C3%A1rios-ds-code-input--docs) | — |
| Etapas | `ds-stepper` | O X-Forms usa a barra do SurveyJS |
| Resumo de erros no topo | `ds-alert` | — |
| **Máscara** (CPF, CEP, telefone) | **Não tem** | No X-Forms, vem do `inputMask` |
| **Colunas e largura por conteúdo** | **Não tem** | Todo campo ocupa 100%: um campo por linha |
| **Opção em card** | **Em criação** | Até lá, use o `ds-radio` |

## Falta componente?

Não crie um componente só para o seu serviço. Peça à SETDIG. O componente novo segue esta ordem:

1. **Confira no Storybook** se ele já existe, às vezes com outro nome.
2. **A X-VIA desenha no Figma**, pelo UX.
3. **O componente entra no Design System**, no Storybook.
4. **Só depois entra na ferramenta** (X-Forms ou Orquestrador).

Assim, o componente fica igual em todo serviço e não precisa ser refeito depois.
