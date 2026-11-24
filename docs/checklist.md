# Checklist do serviço

Confira cada item antes de pedir a homologação. A resposta é **sim**, **não** ou **não se aplica**. Todo **não**
precisa de uma justificativa.

Cada requisito diz **como a SETDIG confere** na homologação. Teste do mesmo jeito antes de pedir.

!!! warning "Em construção"
    Os itens marcados com *a definir com a X-VIA* ainda dependem de como a plataforma expõe o recurso. O
    requisito vale; o "como fazer" entra aqui quando estiver combinado.

## 1. Usa os dados mestres

Cada dado tem **uma fonte oficial** no Estado, como nome e CPF, endereço e data de nascimento. O serviço puxa o dado
dessa fonte. Ele não pede ao cidadão o que o Estado já sabe, nem cria uma cópia própria.

- [ ] O cidadão entra pelo **SmartPass**. O serviço não tem login, senha ou cadastro próprio.
- [ ] Os dados do cidadão logado vêm preenchidos da fonte oficial.
- [ ] O cidadão só digita o que a plataforma não tem.
- [ ] O endereço usa a base de endereço da plataforma, não um campo livre.
- [ ] Pedido feito por outra pessoa (dependente, representante legal) usa o vínculo que a plataforma conhece.
  *A definir com a X-VIA.*

**Como a SETDIG confere:** entra com uma conta de teste e vê se nome, CPF e endereço já chegam preenchidos.

*A lista de dados mestres e quem é dono de cada um: a definir com a X-VIA (apresentação dos dados mestres).*

## 2. Aproveita os recursos do celular

No serviço **nativo** (Orquestrador, dentro do app), use o que o celular já oferece **quando isso poupa trabalho do
cidadão**: localização, câmera para foto de documento e notificações.

- [ ] Se o serviço pede um local, ele oferece "usar minha localização".
- [ ] Se pede foto de documento, ele abre a câmera.
- [ ] O serviço pede a permissão só na hora do uso e diz por quê.
- [ ] O serviço funciona do começo ao fim na tela do celular, sem zoom e sem rolar para o lado.

**Como a SETDIG confere:** faz o pedido inteiro num celular, recusando a permissão uma vez para ver se o serviço
continua.

## 3. Termina com a Avaliação de Serviços

O último passo de todo serviço é a **Avaliação de Serviços**, no modelo do gov.br (Portaria SGD/MGI nº 1.083/2025).

- [ ] Depois de concluir o pedido, o cidadão vê a avaliação.
- [ ] A avaliação é a padrão da plataforma, não uma pesquisa própria do órgão.

**Como a SETDIG confere:** conclui um pedido e vê se a avaliação aparece e chega à plataforma.

## 4. Mostra o status na Minha área

O pedido aparece em **Minha área › Serviços em andamento**, no portal novo e no app, com o status atualizado. Vale
também quando o cidadão não pediu pelo app.

- [ ] Ao enviar, o cidadão vê o **número do pedido** e pode guardar o comprovante.
- [ ] Ao enviar, o pedido aparece em Serviços em andamento.
- [ ] Cada mudança de etapa atualiza o status.
- [ ] O status é escrito para o cidadão (ex.: "Em análise"), não com o código interno.
- [ ] Quando o órgão pede correção ou documento, o cidadão fica sabendo e consegue responder.

**Como a SETDIG confere:** envia um pedido, muda a etapa no lado do órgão e vê o status mudar na Minha área.

*Formato da integração com a Minha área: a definir com a X-VIA.*

## 5. Permite o serviço proativo

A plataforma oferece o serviço **antes de o cidadão pedir**: avisa que a carteira vai vencer, lembra a
renovação, sugere o próximo passo depois de um pedido. Para isso, todo serviço registra o uso (quem usou, qual
serviço, quando e o que foi concedido, com a validade) e a plataforma mostra o aviso em **Sugestões para você**.

- [ ] O serviço envia o evento de uso para a plataforma.
- [ ] O evento traz a data de validade, quando o que foi concedido vence (licença, carteira, certidão).
- [ ] O log não leva dado sensível além do necessário (LGPD).

**Como a SETDIG confere:** conclui um pedido e confere se o evento chegou, com a validade.

*Formato do evento: a definir com a X-VIA.*

## 6. Protege os campos

Todo campo é tratado como entrada não confiável.

- [ ] Todo campo é validado no servidor, além da tela (tipo, tamanho e formato).
- [ ] Consultas ao banco usam parâmetros, nunca texto concatenado (contra SQL injection).
- [ ] O texto digitado é escapado antes de aparecer na tela (contra XSS).
- [ ] Os campos têm limite de tamanho.
- [ ] Os anexos têm tipo e tamanho limitados.
- [ ] O log não guarda CPF, senha, token nem dado de saúde.
- [ ] Se der erro ou um sistema do órgão cair, o cidadão **não perde o que digitou** e a mensagem diz o que fazer.

**Como a SETDIG confere:** digita texto longo, caracteres especiais e anexo grande ou de outro tipo, e vê o serviço
recusar com uma mensagem clara.

## 7. Passa pela homologação com a SETDIG

Nenhum serviço é publicado sem a homologação. Veja [Homologação com a SETDIG](homologacao.md).

- [ ] A X-VIA fez a revisão técnica do código (serviço do Orquestrador).
- [ ] A SETDIG homologou e registrou o aceite.

## Base de todo serviço

Valem para qualquer serviço, junto com os 7 requisitos.

- [ ] A tela usa só componentes do **Design System MS**, sem cor, botão ou campo próprio.
- [ ] O formulário segue o [padrão de formulário](formulario.md).
- [ ] Rótulos, ajudas e mensagens estão em **linguagem simples** (Lei 15.263/2025 e Decreto 16.744/2026).
- [ ] **Acessibilidade:** tudo funciona só pelo teclado, com foco visível, contraste AA e leitura correta no leitor
  de tela.
- [ ] O fim do serviço traz o aviso de privacidade e o termo de ciência, quando há dado pessoal.
- [ ] A carta de serviço está publicada e o botão "Acessar serviço" abre o serviço certo.

**Quando se aplica:**

- [ ] Serviço com taxa: o pagamento usa o meio da plataforma. *A definir com a X-VIA.*
- [ ] Serviço que exige assinatura: usa a assinatura gov.br da plataforma. *A definir com a X-VIA.*
