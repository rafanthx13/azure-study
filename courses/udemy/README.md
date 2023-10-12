# Udemy - Microsoft Azure - Aprenda do Zero

Duração: 9h30min
[Link da Udemy](https://www.udemy.com/course/microsoft-azure-aprenda-do-zero/)


## Introduâo a CLoud

**O que é CLoud COmputing**

Definiçâo do NIST:
+ COmputaçâo emnuvem é um modelo que permite acesso a rede de forma onipresente, conveniente e sob daemanda a um conjunto compartilhado de recursos de computaçâo configuráveis, que podem ser facilmente e rapidamente alocadaos ou liberdados com minimo esforço de gerenciamneto ou interaçao com o prestador de serviço.
+ É um conjeuno de recursos computacionais que podem ser provinados sob demanda rapdiamente

VANTAGESN:
+ mai mobildiades
+ Segurança
+ Escalabidalde: É o pricniapl, voce pode aumetar os recrusos a medida que desejar de forma muito simples. Pay-as-you-Go

## Quando surgiu

+ 1999: SalesForce
+ 2002-2006 - AWS
+ Google Docs 2006
+ Azure 2009

### Nuvem publica/privada/hibrida

publica:
+ É a da AWS/Azure/GCP

private:
+ Seria voce montar sua propria nuvem

Hibrida:
+ Um pedeço do meu negoio move na nuvem publica e os seneiveis na nuvem privada

## Porque usar Azure

+ Pois ela é completa e voce pode alocar serviços bem especificos.
+ DOs maiores player a microsoft é a que tem mais zonas
+ Vantagens
  - Baixo investimento inicial
  - Felxibildiada para experimentar e testar
  - Pagamento por consumo

## Portal antigo e novo da azure: classixo x ARM

classico:
+ manage.windowsazure.com
+ Primeiro protal da azure (surgiu em 2010) e caiu emm desuso em 2015
+ Posusi deploy complexo

ARM - Azure Resource Manager
+ portal.zure.com
+ Orientado a Resoruce Groupps
+ Tme um melhor controle de ACL
+ Permite criar variso recursos ao mesmo tmpo
+ Azure MarketPLace
+ SUporte ao PowerShell & Azure CLI
+ Curiosidades:
  - É possivle mainuplr um conjunto de recuros ao mesmo tempo

## Estrutura do curso

+ 1 . Resource Gorups
+ 2. VNets e SubNets
+ 3. Cirar VMs
+ 4.Criar DB
+ VM com backups
+ Segurança e muita coisa de segurança

NO final você já estará pronto e terá feito um CLOUD DATA CENTER

## 01 - REsoruce Groups

+ Dá para cirar pelo portal ou pelo Power Shell
+ Na azure cada serviço criado estaŕa obrigatoriamente em um RG (ResoruceGroup)Ou será um novo RG ou você colocara em um RG já existete
+ Um recurso so existe em um unico RG, nao temo com o um serviço está em 2 RG ao mesmo tempo
+ Nâo é possível agrupar RG (É como se fosse tuma bolha, um bucket, contianer (nao é cotainer de docker))
+ Não é possível renomear um RG
+ OSs RG nÂo esetão no portal antigo

**Criando um REsourceGorup**
+ VOce define nome, o local fisico (eua brasil india e etcc)
  - TUdo que estiver num RG estará naquele location

IAM = Identity Access Management (chamado de RBAC - role-based access contro)

**Criando no PowerShell**

````
[1] Login-AzureRmAccount   [Loga na conta Azure]

[2] Get-AzureRmResourceGroup  [Lista todos os Grupos de Recursos que existem na Assinatura]

[3] Get-AzureRmLocation | select Location  {Lista todas as localizações possíveis para se criar um grupo de recurso]

[4] New-AzureRmResourceGroup -ResourceGroupName "AZR-EUA" -Location "centralus"  [Cria um Grupo de Recur

]
````

## 02 - VNET

+ O que é uma Vnet (Virtal NEtwork):
  - É uma representaçâo de sua própria rede na nuvem. 
  - Basicmanete é um isolamento lógico na nuvem azure, dedicado à sua asisnatura.
  - VOcê pode conectar Vnest à sua rede local (VPN | Express ROute)

Caracteristicas princiapis
+ Isolmaneto




  - É possǘeil criar N VNert usamd o mesmo bloco de endereços CIDRs
+ SUbnet:
  - Voce pode segmentar uma VNet em múltiplas sub-redes
+ DNS
  - Em geral nâo precisa preocupar com DNS, mesmo asism, eu posso uar um VNet para usar uma DNS interna (isso é mais util em ambeintde cloud hibrida).
  
+ Todas as VNets sâo conectadas à internet por default
+ Os recuross da azure podem usa ra mesma VNet, Nao há necessidade de roteamenteo.
+ As VNets podem se conectadas entre VNets

**Criar VNet via portal**

````
Módulo 7: Exemplo de Comandos Powershell

[1] Login-AzureRmAccount  [Loga na conta Azure]

[2] Get-AzureRmVirtualNetwork -ResourceGroupName AZR-BR

[3] $subnet1 = New-AzureRmVirtualNetworkSubnetConfig -Name "ServersSubnet" -AddressPrefix 10.2.0.0/25

[4] New-AzureRmVirtualNetwork -Name "VNET-AZR-EUA" -ResourceGroupName "AZR-EUA" -Location "centralus" -AddressPrefix 10.2.0.0/24 -Subnet $subnet1
````

## 03 - Azure Virtual Machine

O equivalente ao EC2: É uma máquina com SO livre.

+ A VM é apra quando vocẽ quer um controle bem preciso. Não deve ser a primeira opção apra escolher, há outras também
+ Desvantegem: Tem ue configurar tudo na VM, é uma maquina, um compitardor

Especificaçâo da Azure VM
+ Criar VM no brasil é 35% mais carao que no EUA, por causa de impostoas
+ É cobrado: por hoa, a depdende da VM e do seu HD se é SSD (bom para operaçoes de IO ou HD normal - mais lento, apra uma maquian basica) .

Limite de VM:
+ 20 VMs por regao. Para aumentar tem que entrar em contato com a Azure

+ Parra ter a alta disponibildiade  precisa ter 2 VMS em regioes difenrete oiu nais. Asim a Azreure garnte 99,5% de siponiblidades. Isos é feito ao setar uma opçao na criaçao da VM


**Criando uma VM na azure**:
+ 1 PASSO: BAISCO
+ O que tem que isneirr:
  - Esoclher a image: ubuntu, red hat
  - nome:
  - Tipo do KD: HD ou SSD
   * SSD é mais car, esoclha essa opçâose você quer que tenha lata perfomance quanto a operaçôes de IO
  - Tipó d eautenticaçâo: Pode usar SSH publica ou Senha  (sera uma senha complexa e grande)
  - Subscription: Isos em gerla nao muda, s mudaria se voc/ẽ ffosse uma emrpesa
  - RG ResourceGroup: VOcê seta o RGe autimatiacnte vai pegar o location dlee
+ 2 PASSO: SIZE
  - VOcê esoclhe o tamanho da maquina, e isos incluencia o preço
  - Estude sobre as familias que especificam +- a CPU/MEMORY/HD
+ 3 PASSO: CONFIGURAR
  - Configurar algumas settings da VM:
  - Maaged group? yes/no
  - COnfigurçaoes de rede: Vnet, SUbent, Puclic IP (static/dinamic
  - xtensions: Vários Apps que já podem ser adicionado na maquina

Ao criar, há a opçao de baixa ro template da criaçao da sua maquina, que pdoe ser usando para criar no PowerSHell ou TerraForm

**APos criada**
+ Demora 5minutos pra ela subir
+ VOce acesas ela com Putyy
+ Olhando na oppçoes da VM voce pode setar o size, escolher outro e clcar, em pouoas minutos isso é executado
+ É possível setar o auto-shotdown da máquina

**Criar no PowerSheel - É chato mas da pra fazer**

````sh

Módulo 8: Exemplo de Comandos Powershell

[1] Login-AzureRmAccount  [Loga na conta Azure]

[2] $loc="centralus"
    Get-AzureRMVMImagePublisher -Location $loc | Select PublisherName

[3] $pub="MicrosoftWindowsServer"
    Get-AzureRMVMImageOffer -Location $loc -Publisher $pub | Select Offer

[4] $offer="WindowsServer"
    Get-AzureRMVMImageSku -Location $loc -Publisher $pub -Offer $offer | Select Skus

[5] $sku="2016-Datacenter"
    
[6] Get-AzureRmVMSize -Location $loc [Checar tamanhos de máquinas disponíveis em sua região]
	$vmsize="Standard_A2_v2"

[7] IP_Publico

$rg='AZR-EUA'
$ippub='IP-PUB-WS16-DC-EUA'

$pip = New-AzureRmPublicIpAddress -ResourceGroupName $rg -Location $loc -AllocationMethod Static -IdleTimeoutInMinutes 4 -Name $ippub

[8] NSG | Porta 3389 e 80

$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name Permitir_RDP  -Protocol Tcp `
    -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
    -DestinationPortRange 3389 -Access Allow

$nsgRuleWeb = New-AzureRmNetworkSecurityRuleConfig -Name Permitir_WWW  -Protocol Tcp `
    -Direction Inbound -Priority 1001 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
    -DestinationPortRange 80 -Access Allow

[9] NSG_CRIAÇÃO_DO_NSG

$nsgname='NSG-WS16-DC-EUA'
$nsg = New-AzureRmNetworkSecurityGroup -Name $nsgname -ResourceGroupName $rg -Location $loc -SecurityRules $nsgRuleRDP,$nsgRuleWeb

[10] NIC_CRIAÇÃO_DE_PLACA_DE_REDE_COM_IP_PÚBLICO_CRIADO

$nicname='NIC-WS16-DC-EUA'

$vnet = "VNET-AZR-EUA" 
$vnetinfo = Get-AzureRmVirtualNetwork -Name $vnet -ResourceGroupName $rg | Get-AzureRmVirtualNetworkSubnetConfig -Name "ServersSubnet"
$nic = New-AzureRmNetworkInterface -Name $nicname -ResourceGroupName $rg -Location $loc  -SubnetId $vnetinfo.Id -PublicIpAddressId $pip.Id -NetworkSecurityGroupId $nsg.Id

[11] DEFINIR_UM_OBJETO_DE_CREDENCIAL

$usr = "gmagella"
$pwd =  ConvertTo-SecureString -String "AzureCurso;123" -AsPlainText -Force
$credinfo = New-Object -TypeName "System.Management.Automation.PSCredential" -ArgumentList $usr, $pwd


[12] VM_CARREGAR_CONFIGURAÇÃO_VM

$vmname='WS16-DC-EUA'

$vmConfig = New-AzureRmVMConfig -VMName $vmname -VMSize $vmsize | Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmname -Credential $credinfo | Set-AzureRmVMSourceImage -PublisherName $pub -Offer $offer -Skus $sku -Version latest | Add-AzureRmVMNetworkInterface -Id $nic.Id

[13] CRIAR VM

New-AzureRmVM -ResourceGroupName $rg -Location $loc -VM $vmConfig
````

## 04 - Backp na Azure

### Entendendo Backup

+ Backup inclui backup e restore
+ Hoje em dia é até melhor fazer backup em nuvem do que em local  é mais confiável e barato. 
+ VOcê paga o que usa;  É fácil cresce e dimiuor; criar jobs; 24h com disponibildiade
+ **O AZURE NÃO TEM LIMITE DE TRANFERÊNCIA DE DADOS, E OUTRO TEM** No entanto dve-se usar o 'import/export' da azure par agrandes quantidade de dados. 
  - Criptografia: Voce pode definir uma senha, e fazer o backup. A sneha nao vai junto do backup. Asism, ao dar o restore, só vai funcionar se aplicar essa senha

LRS (Locally Redundant Storage:
+ Cria 3 cópias em 3 locais difenretes na sua regiao; é mais barato
+ GRS (Geo-Redunt Storage: replica seus dados par auma regiao secundária 3 vezes, assim fica 3 copis (3 local e 3 na secundária); é mais caro obviamente

### FOrmas de fazer o bkp

MARS - Azure Backup Agente:
+ Só faz 3 copias por dia; nao reconhece aplicativos; só server em ambiente windows;
+ faz bakup de: arquivos e pastas:
+ Armazena em: Recovery Services Vault

MABS - Azure Backup Server
+ SUporte para liunux; faz bkp d etoda uma VM no VMware; Free
+ Desvantanges:
  - Nao faz bkp dae coisas da Oracle
  - Sempre requer assinatura sempre siponivel
+ Faz bkp de: pastas, arquivos, aplocativos, VMs, VOlumes , Wrok Loads

Backup de VM Iass do Azure
 Nativos as VM WIndows/linux e seus discos; Faz bkp uma vez por dia

+ Microsoft System Center - Data Protection Manager

## 05 - SQL na Azure

+ O banco de dado susadaos por default na Azure como Pass o SQL SERVER. O SQL do azure é totalmente baseado no SQL SERVER entâo é facil passar de um para o outro.
+ O custo do SQL na Azure é definido pelo DTU (meio que uma unidade de medaida de utilziaçao do banco)
+ Na azure há bastante eutenticaçao, firewall e detecçâo de amaeças de invasão na azure, é segura.
+ A porta utilziada para tráfego é a 443

## 06 - Segurnaça na Azure (NSG - Network Security Group)

Equivalnet ea um firewal

+ NSG - rupo de segurança de rede: contemuma lista de segurnaaça euqe permite/nega o tragego de rede para Vnets
+ Podem ser também associados NSG aàs SubRdes, VMs indiiduais além de muitos outros ervços

**como fazer**
+ Nome: Nome da regar 9deve ser unico naquela regiao, o nsg de uma regiao nao pode ser usado nem em outra)
+ Protocolo: TCP, UDP, ou *
+ Poras de origem e de destino: intervlao de peortas de 1 a 65535 ou *
+ Endreço de origem/destino: endereço IP ou sub-rede de IP ou * (todos os endereços
+ DIreçao: Entrada/ou saida
+ Prioriddade: entre 100 e 4096
+ Acess: Permiti ou negar
  -Por default e por questoa de seguraça, a azure descarta tudo que nao se encaixar numa regra de premissao
+ Há regras padrões (elas tem baixa prioridade entoa dá para colcoar regras maisores, mas ao da pra deletalas
  - Rede virutal: o trafego dm um Vnet é permitido nas direçoes de I/O
  - Intenret: É permitido saida para internte mas a entrada é bloqueada
  - Blanceador de carga: Permite trafego para LoadBlaance, manteha se tiver loadblance ou crie uma nova para nao permitir caso nao tiver.
  - As 7:30 há uma tabela que msotra as regras defauls

**COmo usar**
+ O interresanteé definir bem as regra para manter seguro a sua azure. Assim evita ataques DooS.

**Rsmindo**
+ COM a NSG você confiurar os pacotes que entram e sai ddo NSG. qual porta pode ater acessar a internt, po r exemplo, se as portas de bnaco só devem ter acesso a coisa da azure, esse tipo de coisa
+ OBS: NSG nâo é VNET, voce atribui NSG à Vnet
+ A portal do pputy é a porta 22

## 06 - Segurnaça na Azure (RBAC)

Role-Based Access COntrol - RBAC
+ É o gerencimaneto de acesso a usuários.
+ **UM DETERMINADO USUÁRIO DEVE TER A PERMISSÂO MINIMA/ E NECESŚARIA PARA REALISAR AS SUAS ATIVIDADES**
+ Permissâo deais é ruim e permisao de menos pode atrapalhar o funcionário

==> Cada subscription azue está accoaida a m Azure Acitve DIrectory (AAD - mesmo AD da minha compania). Pelo add você atribui via CLI, API, ou portal azuer.

Há 3 funções basicas do RBAC 
+ Proprietario: tem acesos total a tudo e pode delegar acesso
+ COlaborador: pode criar e gerencia r recursos mas nao pode delegar
+ Leitor: Exibe somente recuros existnte, mas nao cria nada. Costuma ser dados a terciero da empresa, que quer só ver as coisas da azure á.

**Significado AD**: Active Directory (AD) is Microsoft's proprietary directory service. It runs on Windows Server and enables administrators to manage permissions and access to network resources. Active Directory stores data as objects. An object is a single element, such as a user, group, application or device such as a printer.

+ Cada assinatura pertece a um AD.
+ UM AD pode ter mais d uma assinatura grenciando
+ Cada RG (grupo de recuros) pertence somente a uma asisnatura
+ Cada recurso pertence somente a um grupo de recursos

**COm fazer**
+ É fieto no IAM.
+ No AD mandamdnos um 'new geust user' e especificamos qual RG e se é READER/colborador. A pessoa nao precisa ter uma subscriçâo nem cadastrar cartao de crédito. É enviadao um email e tem que aceitar.

**se a pesosa sair**
+ voce tem que tirar a permissao e depois remover a pessoa do AD

## 06 - Segurnaça na Azure (Azure Security Centerc - Segurnaça em Cloud)

+ até 2020, 95% das flahas de segurnaça serão causadas pelo usuário final, ou seja, a nuvem tem medidas e pliticas bastante seguras, desde que você as siga.

Azure secutiry center
+ O que faz: monitora a segurança contiualmente; gerenciamnete de segurnaça inteegrado.; detecçao de amaeças e alertas; Funciona com um vasto ecosistema de segurança
+ É um local unificada que ve informaçoes de segurnaça, além de logs
+ Posso definir politicas de segurança
+ COm esas analises continuas agente consegue detectar ciber-ameaças. **MUITO RRO VOCE VAI RECEBER UM FALSO-POSITIVO**. Ele trabalha num nivel pro-ativo.
+ Ela é gratuita, gratuita par aprevençao. Agorade detecçao pdoe ter um custo adiciona. 
+ A azure mostra um dashobars
+ Term um local que informa dicas de segurnaça que você está faltando que devriamimplementar.

 
