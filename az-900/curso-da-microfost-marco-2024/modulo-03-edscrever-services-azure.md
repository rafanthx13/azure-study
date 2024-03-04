# Descrever os tipos de serviço de nuvem

OBS: Resua melhor esa parte

## Objetivos de aprendizagem

Depois de concluir este módulo, você poderá:

Descrever o IaaS (infraestrutura como serviço).
Descrever a PaaS (plataforma como serviço).
Descrever Software como Serviço (SaaS).
Identificar os casos de uso apropriados para cada serviço de nuvem (IaaS, PaaS e SaaS).

## IaaS

O IaaS (infraestrutura como serviço) é a categoria mais flexível de serviços de nuvem, pois oferece o máximo de controle sobre os recursos de nuvem.  Com o IaaS, basicamente o hardware é alugado em um datacenter de nuvem, mas cabe a você decidir o que fazer com ele.

**Responsabildiade do provedor**
+ Em um modelo de IaaS, o provedor de nuvem é responsável por manter o hardware, a conectividade de rede (com a Internet) e a segurança física.

**Responsabildiade do consumidor**: 
+ Você é responsável por todo o resto: instalação, configuração e manutenção do sistema operacional; configuração de rede; configuração de banco de dados e armazenamento e assim por diante. 

No IaaS, a maior parte da responsabilidade fica com você. O provedor de nuvem é responsável por manter a infraestrutura física e o acesso à Internet. Você é responsável por: instalação e configuração, aplicação de patch, atualizações e segurança.

![img-01](imgs/img-01.svg)

## PaaS

O PaaS (Plataforma como serviço) é um meio termo entre alugar espaço em um datacenter (infraestrutura como serviço) e pagar uma solução completa e implantada (software como serviço)

**Responsabildiade do provedor**
m um ambiente de PaaS, o provedor de nuvem mantém a infraestrutura física, a segurança física e a conexão com a Internet. Ele também mantém os sistemas operacionais, o middleware, as ferramentas de desenvolvimento e os serviços de business intelligence que compõem uma solução de nuvem

**Responsabildiade do consumidor**: 
m um cenário de PaaS, você não precisa se preocupar com o licenciamento nem com a aplicação de patch em sistemas operacionais e bancos de dados.

O PaaS é adequado para fornecer um ambiente de desenvolvimento completo sem a preocupação de manter toda a infraestrutura de desenvolvimento.

modeilo de responsabildaide compartihlada

O modelo de responsabilidade compartilhada se aplica a todos os tipos de serviço de nuvem. O PaaS divide a responsabilidade entre você e o provedor de nuvem. O provedor de nuvem é responsável por manter a infraestrutura física e o acesso à Internet, como no IaaS. No modelo de PaaS, o provedor de nuvem também mantém os sistemas operacionais, os bancos de dados e as ferramentas de desenvolvimento. Pense no PaaS como o uso de um computador conectado ao domínio: o departamento de TI mantém o dispositivo com atualizações, patches e renovações regulares.

Dependendo da configuração, você ou o provedor de nuvem pode ser responsável pelas configurações de rede e a conectividade no ambiente de nuvem, a segurança da rede e do aplicativo e a infraestrutura de diretório.

![img-01](imgs/img-01.svg)

## SaaS

O SaaS (software como serviço) é o modelo de serviço de nuvem mais completo do ponto de vista do produto. Com o SaaS, você está essencialmente alugando ou usando um aplicativo totalmente desenvolvido. Email, software financeiro, aplicativos de mensagens e software de conectividade são exemplos comuns de uma implementação de SaaS.

Embora o modelo de SaaS possa ser o menos flexível, ele também é o mais fácil de colocar em funcionamento. Ele requer a menor quantidade de conhecimento técnico ou experiência para o emprego total.

O modelo de responsabilidade compartilhada se aplica a todos os tipos de serviço de nuvem. O SaaS é o modelo que coloca a maior responsabilidade sobre o provedor de nuvem e a menor responsabilidade com o usuário. Em um ambiente de SaaS, você é responsável pelos dados que coloca no sistema, pelos dispositivos que permite que se conectem ao sistema e pelos usuários que têm acesso. Quase todo o resto é responsabilidade do provedor de nuvem. O provedor de nuvem é responsável pela segurança física dos datacenters, pela energia, pela conectividade de rede e pelo desenvolvimento e aplicação de patch dos aplicativos.

## Perugnas

1. Qual tipo de serviço de nuvem é mais adequado para uma migração lift-and-shift de um datacenter local para uma implantação de nuvem? 

IaaS (infraestrutura como serviço)
Com um tipo de serviço de IaaS, você pode aproximar seu ambiente local da nuvem fazendo uma transição lift-and-shift relativamente simples.


PaaS (plataforma como serviço)

SaaS (software como serviço)
2. Em que tipo de serviço de nuvem geralmente estaria uma solução de controle de finanças e despesas? 

IaaS (infraestrutura como serviço)

PaaS (plataforma como serviço)

SaaS (software como serviço)
O SaaS oferece acesso a soluções de software, como controle de despesas e finanças, email ou sistemas de tíquete.