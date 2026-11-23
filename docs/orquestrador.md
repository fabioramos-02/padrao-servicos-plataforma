# Orquestrador

**Quando usar:** um serviço com regra de negócio própria ou tela específica, para órgão com equipe de TI. O
Orquestrador cria o repositório com o microfrontend (a tela) e a regra de negócio. A tela entra no portal ligada à
carta de serviço, pelo botão "Acessar serviço".

## Passo a passo

1. A SETDIG aprova o serviço e conduz a reunião de entendimento com o órgão.
2. A X-VIA cria o ambiente e o repositório pelo Orquestrador.
3. A equipe passa pelo treinamento: Orquestrador, Design System e SmartPass.
4. Desenvolva a tela com os componentes do **Design System MS** e o [padrão de formulário](formulario.md).
5. Atenda os [7 requisitos](checklist.md), com atenção aos que só valem aqui:
    - recursos do celular no serviço nativo;
    - validação no servidor e consultas com parâmetros;
    - status em Serviços em andamento e log de uso.
6. Entregue o código para a revisão técnica da X-VIA (repasse técnico).
7. Peça a [homologação](homologacao.md) à SETDIG.

## Combinados que valem para todo microfrontend

- Login sempre pelo **SmartPass**. Nada de login próprio.
- Os dados do cidadão vêm dos dados mestres, não de uma base própria.
- O serviço não guarda dado pessoal além do que precisa para funcionar.
- A tela segue o mesmo cabeçalho, trilha e rodapé do portal.

*Templates de microfrontend e a integração com o CMS: a definir com a X-VIA (proposta de fluxo do Kauã).*
