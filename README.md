# Controle de campanhas F360

### Nota: Toda e qualquer atualização feita dentro do repositório do github não atualiza automáticamente, então após subir as alterações espere alguns minutos para que seja efetivado no sistema.

### O que é uma campanha por meio de popup

As utilizamos as campanhas na F360 para divulgar **cursos**, **novidades**, **campanhas**, **alertas**, entre outros. 

As campanhas por **regra** possuem uma imagem obrigatoriamente, um link (CTA) onde direcionamos o click do cliente para ter mais informações sobre a campanha (em alguns casos não possui cta).

### O que fazer para configurar uma nova campanha?

O primerio passo é incluir a imagem dentro da pasta **Imagens** do repositório e após isso incluir os parâmetros e configuração da campanha no arquivo exemplo.json.

### Como adicionar imagem?

Dentro da pasta Imagens tem um botão no canto superior à direita **Add file** (adicionar arquivo), onde ao clicar vai aparecer duas opções: **Create new file** e **Upload files**. Selecione Upload files para incluir o arquivo e clique em **Commit changes**.


### Como configurar e o que são as propriedades do arquivo .json e para qeu serve?

No arquivo .json temos as propriedades:

- nome: somente o nome do popup,
- imagem: o link da imagem do proprio github, onde voce fez o upload anteriormente,
- "link": é o cta, link de redirecionamento,
- "localStorageId": é um identificador para os popups que ja foram visualizados pelo cliente,
- "categoria": é o nome da campanha no analytics,
- "inicio": quando se inicia a campanha (importante estar no mesmo formato),
- "fim": quando finaliza a campanha (importante estar no mesmo formato),
- "action": nome da ação realizada pelo cliente no analytics,
- "preventClient": lista de cliente que devemos prevenir a visualização formato ["cliente", "cliente 2"],
- "preventCli": lista de CLI que devemos prevenir a visualização formato ["cli-4512", "clo-4512"],
- "direcionarCampanha": lista de clientes que irão visualizar a campanha ["tes-4512", "clo-4512"], caso não tenha um direcionamento colocar [],
- "closeColor": caso queira diferenciar a cor do botão de acordo com a imagem da campanha

Importante nunca colocar duas campanhas no mesmo periodo, pois iremos sempre colocar a primeira para aparecer e também não repetir localStorageId, pois deve ser um identificador único.

