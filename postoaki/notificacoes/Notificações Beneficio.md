**data** 22/11/2024
## O que foi construído 

1. Revisão da geração do código promocional para o voucher avulso por notificação.
2. Buscar GrupoEmpresaMin, GrupoEmpresaUsuarioMin, VoucherMinDto, GrupoDescontoMinDto, NotificacaoAppMinDto
3. configuração modalidade de código
4. consultar se código ja existe
5. criar Voucher Item
6. geração de código
7. teste e correções (erros)
8. configurar load app ao gerar código
9. erro ao gerar código, [existe dados semelhantes] 

**data** 25/11/2024 

**O que fazer**:
1. Testar no PDV, se esta aplicando desconto ou pontuação de acordo com o grupo de desconto. ()==ok==
2. Verificar o respeito dos limites.
3.  Definir ordem dos cupons.
4. 'Trata' os cupons utilizados.
5.  Verificar sobre Notificações que são deletadas.


Feito:
1. Ajuste ajustar grupo desconto de acordo com a notificação. Não estava aplicando desconto da Notificação no voucher notificação
2. Ajuste dos limites, não está respeitando os limites de acordo com o grupo de desconto da notificação. Resgatei uma att que resolvia isso. Branche deletada. Card defct-14648(contém bugs)


**data**: 26/11/2024


**O que fazer**:.
-  Definir ordem dos cupons. ==**ok**==
- Editar UI dos cupons de acordo com status. ==ok== 
- Verificar sobre Notificações que são deletadas. ==Ok==
- Testar envios por outros canais de envio 
- Enviar notificação com Grupo Desconto que pontua. **==OK==**
- Verificar limite, se respeita o do Voucher **==ok==**


Não esta respeitando a fidelização do Grupo de Desconto do Voucher/notificação. Está respeitando do Código usuário ==OK==

Respeita o limite de acordo com o Grupo de desconto para voucher avulso. Mas para gerar no App diz que ja atingiu o limite do Grupo do usuário ==ok==

Filtros cupoms [utilizados, expirados, disponíveis,todos]- front/back **==ok==** 


**data**: 28/11/2024

Veficação cupons por email ==ok==
Veficação cupons por sms ==ok==

enviar consulta de regras para detalhes cupom ==ok==
gerar QrCode. ==ok==
priorizar cupons disponives ==ok==
Empty message cupons. ==ok==
erro no servidor ao gerar cupom posto ==ok==
remover botão de resgate quando já utilizado.==ok==
tentar remover regras da chamada dos cupons e levar em detalhes ==ok==
atalho para cupom nos links-personalizados ==ok==


**data**: 29/11/2024
verificar com Bdados para optmizar a consulta ==ok==
criar migration ==ok==
verificar detalhes notificações ==ok==
inserir busca por uuid de cupom ==ok==
redirect from details to details ==ok==

**data**: 02/12/2024
Informar os status no cupom Details ==ok==
tradução APP ==ok==
bug- carregando duas vezes ==ok== PS: Criei um util no loadService **isLoading**. Verifica se esta em loading.
bug - link personalizado em SERVIÇO redirect. ==OK==
bug - gerando código infinitamente ==ok==


**data**:03/12/2024
aviso prévio de non-delete notificação   ==ok==
erro envio em massa ==ok==
error agendar[testada todas as agendadas] ==ok==


**data**: 04/12/2024
agendadas não esta gerando voucher[317-NotificacaoPainelService] ==ok==
tootip descrição cupom e regras ==ok==

## TESTAR

==RETORNAR A VALIDADACAO DATA AGENDAMENTO==
- Testar rotas dos links personalizados e serviço ()
- ATENÇÃO A PERDA DE VINCULO DA NOTIFICACAO COM USER
MY PLAY_ID_GOOGLE: **6e5b6054-e26a-4dc2-972c-97df7e0deb49**