# Orquestrador

**Quando usar:** um serviço com regra de negócio própria ou tela específica, para órgão com equipe de TI. A equipe do
órgão cria o repositório pelo Orquestrador, com o microfrontend (a tela) e a regra de negócio. A tela entra no portal
ligada à carta de serviço, pelo botão "Acessar serviço".

## Passo a passo

1. A SETDIG aprova o serviço e conduz a reunião de entendimento com o órgão.
2. A equipe passa pelo treinamento: Orquestrador, Design System e SmartPass.
3. **Peça acesso ao GitLab** pela carta de serviço
   [Conceder acesso ao GitLab](https://www.ms.gov.br/ciencia-e-tecnologia/conceder-acesso-ao-gitlabs17), do seu e-mail
   institucional. No primeiro acesso, crie a sua própria senha. A CSI-EAST põe você como Developer no subgrupo do seu
   órgão, por exemplo `XVIA/orgaos/sefaz`. O GitLab só abre na rede do Governo ou pela VPN.
4. **Crie o repositório pelo Orquestrador**, com o login do GitLab. Escolha o template: Frontend Next.js (tela no
   portal) ou Backend NestJS (API). Use um nome que nenhum outro órgão use. O repositório nasce privado, com a pipeline
   e o Design System prontos. Depois de clonar, rode `node scripts/initialize.mjs`.
5. Desenvolva a tela com os [componentes do formulário](componentes.md) do **Design System MS** (os mesmos do
   X-Forms) e o [padrão de formulário](formulario.md).
6. Atenda os [7 requisitos](checklist.md), com atenção aos que só valem aqui:
    - recursos do celular no serviço nativo;
    - validação no servidor e consultas com parâmetros;
    - status em Serviços em andamento e o evento de uso que permite o serviço proativo.
7. Trabalhe numa branch sua e abra merge request. A `develop` publica em desenvolvimento, a `homolog` em homologação e
   a `main` em produção. O mantenedor do subgrupo aceita o merge, e a pipeline testa, analisa e publica.
8. Entregue o código para a revisão técnica da X-VIA (repasse técnico).
9. **Ligue a carta à tela no CMS.** A carta precisa ter uma etapa digital. Nessa etapa, marque o serviço como interno
   e escolha o microfrontend. O CMS só publica a carta depois que o microfrontend foi publicado.
10. Peça a [homologação](homologacao.md) à SETDIG.

## Combinados que valem para todo microfrontend

- Login sempre pelo **SmartPass**. Nada de login próprio.
- Os dados do cidadão vêm dos dados mestres, não de uma base própria.
- O serviço não guarda dado pessoal além do que precisa para funcionar.
- A tela segue o mesmo cabeçalho, trilha e rodapé do portal.
- O repositório é sempre **privado**. Nunca "Internal": com essa opção, qualquer pessoa logada no GitLab do Estado vê o
  código.
- Os segredos da pipeline ficam com a X-VIA. O órgão não vê nem cadastra.

Exemplo no ar (ambiente de desenvolvimento):
[Consultar delegacias e endereços](https://portal.dev.pgd.ms.gov.br/app/consultar-delegacias-e-enderecos), feito no
Orquestrador com os componentes do Design System.

Regras completas de acesso, grupos e segredos:
[Governança do Orquestrador e do acesso ao Design System](https://docs.google.com/document/d/1kSKsbJ3RTFWfbVw4Ix550Z_S72pQz7PNl-xmdzMnqw0/edit)
(documento da SGD).
