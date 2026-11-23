# X-Forms

**Quando usar:** um serviço que é um pedido com formulário e um caminho de análise dentro do órgão, sem
integração com sistema. O órgão monta na tela (X-Forms Designer + X-Flows) e publica a carta no CMS.

!!! warning "O Testar questionário não é o que o cidadão vê"
    Ele roda o SurveyJS puro, com outro tema e outro layout. Confira sempre no **Visualizar**.
    Veja [Formulário: o que o cidadão vê](formulario-renderizacao.md).

## Passo a passo

1. Peça o acesso ao Designer pela SETDIG.
2. Monte o formulário seguindo o [padrão de formulário](formulario.md).
3. Ligue os campos aos **dados mestres** (CPF, nome, endereço), em vez de pedir de novo.
4. Configure o fluxo no X-Flows: quem analisa cada etapa e qual status o cidadão vê em cada uma.
5. Inclua no fim o aviso de privacidade, o termo de ciência e a **Avaliação de Serviços**.
6. Confira o [checklist](checklist.md) e peça a [homologação](homologacao.md).

## O que muda no X-Forms

| Requisito | No X-Forms |
|---|---|
| Recursos do celular | Em geral não se aplica (é web) |
| Proteção dos campos | Use os tipos e as máscaras do X-Forms (CPF, e-mail, data) e os limites de tamanho |
| Status na Minha área | Vem das etapas do X-Flows. Dê a cada etapa um nome que o cidadão entenda |

Manual do X-Forms: [Estudo de Formulários › Manual do X-Forms](https://fabioramos-02.github.io/estudo-formularios/xforms-manual/).
