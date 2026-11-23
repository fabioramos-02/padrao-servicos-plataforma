# Checklist do serviço

Confira cada item antes de pedir a homologação. A resposta é **sim**, **não** ou **não se aplica**. Todo **não**
precisa de uma justificativa.

!!! warning "Em construção"
    Os itens marcados com *a definir com a X-VIA* ainda dependem de como a plataforma expõe o recurso. O
    requisito vale; o "como fazer" entra aqui quando estiver combinado.

## 1. Usa os dados mestres

Cada dado tem **uma fonte oficial** no Estado, como nome e CPF, endereço e data de nascimento. O serviço puxa o dado
dessa fonte. Ele não pede ao cidadão o que o Estado já sabe, nem cria uma cópia própria.

- [ ] Os dados do cidadão logado vêm preenchidos da fonte oficial.
- [ ] O cidadão só digita o que a plataforma não tem.
- [ ] O endereço usa a base de endereço da plataforma, não um campo livre.

*A lista de dados mestres e quem é dono de cada um: a definir com a X-VIA (apresentação dos dados mestres).*

## 2. Aproveita os recursos do celular

No serviço **nativo** (Orquestrador, dentro do app), use o que o celular já oferece **quando isso poupa trabalho do
cidadão**: localização, câmera para foto de documento e notificações.

- [ ] Se o serviço pede um local, ele oferece "usar minha localização".
- [ ] Se pede foto de documento, ele abre a câmera.
- [ ] O serviço pede a permissão só na hora do uso e diz por quê.

## 3. Termina com a Avaliação de Serviços

O último passo de todo serviço é a **Avaliação de Serviços**, no modelo do gov.br (Portaria SGD/MGI nº 1.083/2025).

- [ ] Depois de concluir o pedido, o cidadão vê a avaliação.
- [ ] A avaliação é a padrão da plataforma, não uma pesquisa própria do órgão.

## 4. Mostra o status na Minha área

O pedido aparece em **Minha área › Serviços em andamento**, no portal novo e no app, com o status atualizado. Vale
também quando o cidadão não pediu pelo app.

- [ ] Ao enviar, o pedido aparece em Serviços em andamento.
- [ ] Cada mudança de etapa atualiza o status.
- [ ] O status é escrito para o cidadão (ex.: "Em análise"), não com o código interno.

*Formato da integração com a Minha área: a definir com a X-VIA.*

## 5. Gera log para o "Sugestões para você"

O serviço registra o uso (quem usou, qual serviço, quando) para a plataforma sugerir os próximos serviços ao
cidadão.

- [ ] O serviço envia o evento de uso para a plataforma.
- [ ] O log não leva dado sensível além do necessário (LGPD).

*Formato do evento: a definir com a X-VIA.*

## 6. Protege os campos

Todo campo é tratado como entrada não confiável.

- [ ] Todo campo é validado no servidor, além da tela (tipo, tamanho e formato).
- [ ] Consultas ao banco usam parâmetros, nunca texto concatenado (contra SQL injection).
- [ ] O texto digitado é escapado antes de aparecer na tela (contra XSS).
- [ ] Os campos têm limite de tamanho.
- [ ] Os anexos têm tipo e tamanho limitados.

## 7. Passa pela homologação com a SETDIG

Nenhum serviço é publicado sem a homologação. Veja [Homologação com a SETDIG](homologacao.md).

- [ ] A SETDIG homologou e registrou o aceite.

## Também conta

- [ ] O formulário segue o [padrão de formulário](formulario.md).
- [ ] O fim do serviço traz o aviso de privacidade e o termo de ciência, quando há dado pessoal.
- [ ] A carta de serviço está publicada e aponta para o serviço.
