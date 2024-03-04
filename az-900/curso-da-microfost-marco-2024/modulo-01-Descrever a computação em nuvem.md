# Módulo 1

## Index

Descrever a computação em nuvem
23 min
Módulo
8 Unidades
Iniciante
Administrador
Desenvolvedor
Engenheiro de DevOps
Arquiteto de Soluções
Azure
Este módulo apresenta a computação em nuvem. Ele aborda coisas como conceitos de nuvem, modelos de implantação e compreensão da responsabilidade compartilhada na nuvem.

Objetivos de aprendizagem
Ao concluir este módulo, você será capaz de:

Definir computação em nuvem.
Descrever o modelo de responsabilidade compartilhada.
Definir modelos de nuvem, incluindo público, privado e híbrido.
Identificar os casos de uso apropriados para cada modelo de nuvem.
Descrever o modelo baseado no consumo.
Comparar os modelos de preços de nuvem.
Pré-requisitos
Familiaridade básica com termos e conceitos de TI
Este módulo faz parte destes roteiros de aprendizagem

Princípios básicos do Microsoft Azure: descrever os conceitos de nuvem
Introdução aos conceitos básicos do Microsoft Azure
2 min
Introdução à computação em nuvem
1 min
O que é computação em nuvem
3 min
Descrever o modelo de responsabilidade compartilhada
3 min
Definir os modelos de nuvem
4 min
Descrever o modelo baseado em consumo
3 min
Verificação de conhecimentos
5 min
Resumo
2 min

## Porque estudar o basico da azure, par ao AZ-900 pois... 

| Área de domínio do AZ-900                         | Weight   |
|---------------------------------------------------|----------|
| Descrever os conceitos da nuvem                   | 25-30%   |
| Descrever a arquitetura e os serviços do Azure    | 35 a 40% |
| Descrever o gerenciamento e a governança do Azure | 30 a 35% |

## Introdução à computação em nuvem

Concluído
100 XP
1 minuto

Neste módulo, você conhecerá os conceitos gerais de nuvem. Você começará com uma introdução à nuvem em geral. Em seguida, você se aprofundará em conceitos como responsabilidade compartilhada, diferentes modelos de nuvem e explorará o método de preço exclusivo da nuvem.

Se você já estiver familiarizado com a computação em nuvem, este módulo poderá ser uma ampla revisão para você.

## Objetivos de aprendizagem

Depois de concluir este módulo, você poderá:

Definir computação em nuvem.
Descrever o modelo de responsabilidade compartilhada.
Definir modelos de nuvem, incluindo público, privado e híbrido.
Identificar os casos de uso apropriados para cada modelo de nuvem.
Descrever o modelo baseado no consumo.
Comparar os modelos de preços de nuvem.

## O que é computação em nuvem - cloud computing

A computação em nuvem é a entrega de serviços de TI pela Internet, que incluem infraestrutura como máquinas virtuais, armazenamento, bancos de dados e rede. Além dos serviços tradicionais, a nuvem oferece recursos como IoT, machine learning e inteligência artificial. Diferentemente de um datacenter físico, a nuvem não está limitada por infraestrutura física, permitindo escalabilidade rápida sem a necessidade de construir novos datacenters.

As

## Descrever o modelo de responsabilidade compartilhada

Responsabilidades do provedor de nuvem:

1. Datacenter físico
2. Rede física
3. Hosts físicos

Responsabilidades do consumidor:

1. Informações e dados armazenados na nuvem
2. Dispositivos e usuários com permissão para se conectar à nuvem (ex: telefones celulares, computadores)
3. Contas e identidades das pessoas, serviços e dispositivos na organização

Além disso, o modelo de serviço determina a responsabilidade por aspectos como sistemas operacionais, controles de rede, aplicativos e infraestrutura de identidade.

Ex de um caso: Se ocê usa um banco da cloud, a cloud gerencia a manutnçao do banco. Agora se você instlar o mysql em uma VM, aí é você que fica a cargo da manutenção

## Definir modelos de nuvem

Nuvem privada

Uma nuvem privada é, de certa forma, a evolução natural de um datacenter corporativo. Ela é uma nuvem (que fornece serviços de TI pela Internet) usada por uma única entidade. A nuvem privada fornece um controle muito maior para a empresa e o departamento de TI. No entanto, ela também tem mais custos e menos benefícios em relação a uma implantação de nuvem pública. Por fim, uma nuvem privada pode ser hospedada em seu datacenter local. Ela também pode ser hospedada em um datacenter dedicado externo, até mesmo por terceiros que tenham dedicado esse datacenter à sua empresa.

Nuvem pública

Uma nuvem pública é criada, controlada e mantida por um provedor de nuvem de terceiros. Com uma nuvem pública, qualquer pessoa que queira comprar serviços de nuvem pode acessar e usar os recursos. A disponibilidade pública geral é uma diferença fundamental entre nuvens públicas e privadas.

Nuvem híbrida
Uma nuvem híbrida é um ambiente de computação que usa nuvens públicas e privadas em um ambiente interconectado. Um ambiente de nuvem híbrida pode ser usado para permitir que uma nuvem privada escale para atender a uma demanda maior temporária implantando recursos de nuvem pública. A nuvem híbrida pode ser usada para fornecer uma camada adicional de segurança. Por exemplo, os usuários podem escolher com flexibilidade quais serviços manter na nuvem pública e quais implantar na infraestrutura de nuvem privada.

| Área de domínio do AZ-900                                              | Weight                                                                            |                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Nuvem pública                                                          | Nuvem privada                                                                     | Nuvem híbrida                                                                 |
| Nenhuma despesa de capital para escalar verticalmente                  | As organizações têm controle total sobre os recursos e a segurança                | Fornece a maior flexibilidade                                                 |
| Os aplicativos podem ser provisionados e desprovisionados rapidamente  | Os dados não são colocados com os dados de outras organizações                    | As organizações determinam o local para executar os aplicativos               |
| As organizações pagam apenas pelo que utilizam                         | O hardware deve ser comprado para o início e a manutenção                         | As organizações controlam a segurança, a conformidade ou os requisitos legais |
| As organizações não têm controle total sobre os recursos e a segurança | As organizações são responsáveis pela manutenção e pelas atualizações de hardware |                                                                               |

4ª cenário: usar várias nuvens publics,,a ex, aws  + gcp

=> **Azure Arc**

O Azure Arc é um conjunto de tecnologias que ajuda a gerenciar seu ambiente de nuvem. O Azure Arc pode ajudar a gerenciar o seu ambiente de nuvem, seja uma nuvem pública exclusivamente no Azure, uma nuvem privada em seu datacenter, uma configuração híbrida ou até mesmo um ambiente de várias nuvens em execução em vários provedores de nuvem ao mesmo tempo.

## Descrever o modelo baseado em consumo

A computação em nuvem se enquadra na OpEx ( OpEx (despesas operacionais).) porque opera em um modelo baseado em consumo. Na computação em nuvem, você não paga pela infraestrutura física, pela eletricidade, pela segurança nem por nada que esteja associado à manutenção de um datacenter. Você paga pelos recursos de TI que usa. Se você não usar nenhum recurso de TI durante o mês, não pagará nada.

Um modelo baseado em consumo oferece vários benefícios, como:

Sem custos prévios.
Não há necessidade de comprar nem gerenciar uma infraestrutura cara que os usuários talvez não usem na capacidade máxima.
A capacidade de pagar para obter mais recursos quando necessário.
A capacidade de parar de pagar por recursos que não são mais necessários.
Com um datacenter tradicional, você tenta estimar as necessidades futuras de recursos. Se você superestimar, gastará mais do que o necessário no datacenter, podendo desperdiçar capital. Se você subestimar, o datacenter atingirá a capacidade rapidamente e os aplicativos e serviços poderão sofrer redução de desempenho. A correção de um datacenter subprovisionado pode ser muito demorada. Pode ser necessário solicitar, receber e instalar mais hardware. Você também precisará adicionar energia, resfriamento e rede para o hardware extra.

Em um modelo baseado em nuvem, você não precisa se preocupar em acertar perfeitamente as necessidades de recursos. Se você achar que precisa de mais máquinas virtuais, bastará adicioná-las. Se a demanda cair e você não precisar de tantas máquinas virtuais, bastará remover algumas, conforme o necessário. De qualquer forma, você só paga pelas máquinas virtuais que usa, não pela "capacidade extra" que o provedor de nuvem tem em mãos.

Computação em nuvem é a entrega de serviços de computação pela Internet, usando o modelo de preço pago conforme o uso. Normalmente, você paga apenas pelos serviços de nuvem que usa, o que ajuda a:

+ Planeje e gerencie os custos operacionais.
+ Executar a infraestrutura com mais eficiência.
+ Escale as operações de acordo com as necessidades de negócios.

Em outras palavras, a computação em nuvem é uma forma de alugar capacidade computacional e armazenamento do datacenter de terceiros. Você pode tratar os recursos de nuvem como faria com os recursos em seu próprio datacenter. Mas, ao contrário do seu próprio datacenter, ao terminar de usar os recursos de nuvem, basta devolvê-los. Você é cobrado apenas pelo que usa.

Em vez de manter CPUs e armazenamento no seu datacenter, você aluga esses recursos pelo tempo necessário. O provedor em nuvem é responsável por manter a infraestrutura subjacente para você. A nuvem permite que você supere rapidamente os desafios empresariais mais difíceis e ofereça soluções de ponta para seus usuários.