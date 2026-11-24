# Referências

O padrão não nasceu do zero. Cada regra vem de uma fonte que já foi testada com o cidadão. A tabela diz **o que
adotamos** de cada uma e onde a regra está detalhada.

## O que adotamos de cada fonte

| Fonte | O que adotamos | Onde está a regra |
|---|---|---|
| [GOV.UK Service Standard](https://www.gov.uk/service-manual/service-standard) | Um padrão único para todo serviço e avaliação antes de publicar | [Checklist](checklist.md) e [homologação](homologacao.md) |
| [GOV.UK — Question pages](https://design-system.service.gov.uk/patterns/question-pages/) | Pergunta que muda o caminho fica sozinha na página; área do formulário com no máximo dois terços da tela | [Diagramação](https://fabioramos-02.github.io/estudo-formularios/01-diagramacao/) |
| [GOV.UK Design System — padrões](https://design-system.service.gov.uk/patterns/) | Como pedir nome, data, e-mail e telefone; dizer por que pede o dado; não corrigir a grafia do nome | [Recomendações GOV.UK](https://fabioramos-02.github.io/estudo-formularios/andamento/recomendacoesGOVUK/) |
| gov.br — boas práticas de formulário | Coluna única; nada de layout em várias colunas | [Diagramação](https://fabioramos-02.github.io/estudo-formularios/01-diagramacao/) |
| [gov.br — Avaliação de serviços](https://www.gov.br/governodigital/pt-br/transformacao-digital/central-de-qualidade) | Avaliação padrão no fim do serviço (Portaria SGD/MGI nº 1.083/2025) | [Checklist, requisito 3](checklist.md#3-termina-com-a-avaliacao-de-servicos) |
| NN/g — Website forms usability (2016) | Uma coluna: várias colunas quebram o movimento de descer pelo formulário | [Diagramação](https://fabioramos-02.github.io/estudo-formularios/01-diagramacao/) |
| Área logada (Minha área) do portal novo | Serviços em andamento, com o status de cada pedido, e dados do cidadão vindos dos dados mestres | [Checklist, requisitos 1 e 4](checklist.md) |
| Design System MS (`@plataforma-xvia/ds-react`) | Componentes, ajuda abaixo do campo, contador de caracteres, etapas | [Formulário: o que o cidadão vê](formulario-renderizacao.md) |
| Lei 15.263/2025 e Decreto 16.744/2026 | Linguagem simples em rótulos, ajudas e mensagens | [Formulário](formulario.md) |
| [Estudo de Formulários](https://fabioramos-02.github.io/estudo-formularios/) | O padrão de formulário do X-Forms, testado nos 14 formulários da SETDIG | [Formulário](formulario.md) |

## Campos e áreas: o que fica padronizado

| Ponto | Regra | Fonte |
|---|---|---|
| Coluna | Um campo por linha, sempre | gov.br, GOV.UK, NN/g |
| Largura | A caixa tem o tamanho da resposta: CEP e número curtos, nome e e-mail longos. Texto longo usa caixa de várias linhas | GOV.UK |
| Área do formulário | No máximo dois terços da tela no computador e a largura toda no celular | GOV.UK |
| Limite de caracteres | Todo campo tem limite, conferido também no servidor; texto longo mostra o contador | DS MS, [checklist, requisito 6](checklist.md#6-protege-os-campos) |
| Espaço entre campos | O do DS MS, sem espaçamento próprio | DS MS |
| Ajuda e erro | Abaixo do campo, no mesmo lugar | DS MS |
| Agrupamento | Etapas por assunto, com cerca de 8 campos cada, e título que diz o que se pede | GOV.UK, Estudo de Formulários |
| Obrigatório | Asterisco no obrigatório e "(opcional)" no rótulo do opcional | Estudo de Formulários |
| Botões | Um botão principal por etapa, com verbo: "Continuar" e, no fim, "Enviar solicitação" | GOV.UK |

O que o Design System ainda não tem (largura por conteúdo, máscara e grupo de radio) está em
[Formulário: o que o cidadão vê](formulario-renderizacao.md#o-design-system-ja-tem-os-componentes).
