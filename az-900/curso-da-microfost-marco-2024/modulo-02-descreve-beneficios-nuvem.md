# Descrever os benefícios do uso de serviços de nuvem

Neste módulo, você conhecerá alguns dos benefícios oferecidos pela computação em nuvem. Você aprenderá como a computação em nuvem pode ajudar a atender à demanda variável e ainda oferecer uma ótima experiência ao cliente. Você também aprenderá sobre segurança, governança e capacidade de gerenciamento geral na nuvem.

## Objetivos de aprendizagem

Depois de concluir este módulo, você poderá:

-   Descrever os benefícios da alta disponibilidade e da escalabilidade na nuvem.
-   Descrever os benefícios da confiabilidade e da previsibilidade na nuvem.
-   Descrever os benefícios da segurança e da governança na nuvem.
-   Descrever os benefícios da capacidade de gerenciamento na nuvem.
-   
### Benficio 1: Alta Disponibildiade

A alta disponibilidade se concentra em garantir a disponibilidade máxima, independentemente de interrupções ou eventos que possam ocorrer.

O Azure é um ambiente de nuvem altamente disponível com garantias de tempo de atividade, dependendo do serviço. Essas garantias fazem parte dos SLAs (Contratos de Nível de Serviço)

Em um vídos: fala da difenreça entre o SLA de 99% eo da Aure que é de 99,95. O 99 pode ficar 1.68 horas fora do ar por semana ou ainda 7,2horas por mes e está dentro do 99%., um com 99,99% fica 10minutos por semana ou 42 minutos poir mes. Perceba a difenreça mensal, entre 40 minutos para  7 horas. Se seu serviço for critic isso pdoe fazer a difenreça. Lembrando que cada serviço da azure tem o seu próprio SLA

### Beneficio 2: Escalabidildaide

A escalabilidade refere-se à capacidade de ajustar recursos para atender à demanda. Se você experimentar um pico repentino de tráfego e seus sistemas ficarem sobrecarregados, a capacidade de escalar significa que você poderá adicionar mais recursos para lidar melhor com o aumento da demanda.

O outro benefício da escalabilidade é que você não está pagando além do necessário pelos serviços. Como a nuvem é um modelo baseado em consumo, você paga apenas pelo que usa. Se a demanda cair, você poderá reduzir seus recursos e, assim, reduzir seus custos.

A escala geralmente vem em duas variedades: vertical e horizontal. 

A escala vertical se concentra em aumentar ou diminuir a capacidade dos recursos. 
+ Com a escala vertical, se você estivesse desenvolvendo um aplicativo e precisasse de mais capacidade de processamento, poderia escalar verticalmente para adicionar mais CPUs ou RAM à máquina virtual. Por outro lado, se você percebesse que superestimou as necessidades, poderia reduzir verticalmente, diminuindo as especificações de CPU ou RAM.

A escala horizontal é adição ou subtração do número de recursos.
+ Com a escala horizontal, se você experimentasse um salto repentino acentuado na demanda, seus recursos implantados poderiam ser expandidos (automaticamente ou manualmente). Por exemplo, você pode adicionar máquinas virtuais ou contêineres por meio da expansão. Da mesma forma, se houver uma queda significativa na demanda, os recursos implantados poderão ser reduzidos horizontalmente (de maneira automática ou manual).
## Outros beneficios
+ 
1. **Confiabilidade:**
   - **Resumo:** A nuvem Azure oferece confiabilidade e resiliência através de um design descentralizado e global. Com recursos implantados em várias regiões do mundo, mesmo em caso de eventos catastróficos em uma região, outras regiões permanecerão em funcionamento. A escala global da Azure permite que os aplicativos aproveitem automaticamente essa confiabilidade, podendo, em alguns casos, mudar automaticamente para uma região diferente sem intervenção manual.
   
2. **Previsibilidade:**
   - **Resumo:** A previsibilidade na nuvem Azure proporciona confiança avançada, seja em termos de desempenho ou de custos. Soluções construídas com base no Microsoft Azure Well-Architected Framework garantem tanto custos quanto desempenho previsíveis. Isso é possível através de uma implementação que segue a estrutura mencionada, oferecendo assim um ambiente com custos e desempenho que podem ser antecipados.

3. **Desempenho:**
   - **Resumo:** A previsibilidade de desempenho na nuvem Azure está relacionada à capacidade de prever os recursos necessários para proporcionar uma experiência satisfatória aos usuários. Conceitos como dimensionamento automático, balanceamento de carga e alta disponibilidade são fundamentais para garantir essa previsibilidade. O dimensionamento automático permite a implantação de recursos adicionais quando há aumento na demanda, enquanto o balanceamento de carga redistribui o tráfego para áreas menos congestionadas, assegurando um desempenho estável.

4. **Custo:**
   - **Resumo:** A previsibilidade de custos na nuvem Azure foca na capacidade de prever os gastos com a nuvem. Com ferramentas de monitoramento em tempo real e análise de dados, é possível acompanhar e otimizar o uso de recursos, além de identificar padrões e tendências para planejar implantações futuras de forma mais eficiente. Utilizando análises e informações da nuvem, os usuários podem prever custos futuros e ajustar os recursos conforme necessário, utilizando ferramentas como TCO (custo total de propriedade) ou a Calculadora de Preços para estimativas precisas.
 - 5. Segurnaça
 -  - E como a nuvem se destina a uma entrega de recursos de TI via Internet, os provedores de nuvem normalmente são adequados para lidar com situações como ataques de DDoS (negação de serviço distribuído), tornando sua rede mais robusta e segura.
-  ## Gerenciamneto: na nuvem e da nuvem
-  


## Gerenciamento da nuvem

O gerenciamento da nuvem diz respeito a gerenciar seus recursos de nuvem. Na nuvem, você pode:

-   Escalar automaticamente a implantação de recursos com base na necessidade.
-   Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual.
-   Monitorar a integridade dos recursos e substituir automaticamente os recursos com falha.
-   Receber alertas automáticos com base em métricas configuradas, de modo a ficar ciente do desempenho em tempo real.

## Gerenciamento na nuvem

O gerenciamento na nuvem diz respeito à maneira de gerenciar seu ambiente de nuvem e seus recursos. Você pode gerenciá-los:

-   Por meio de um portal da Web.
-   Usando uma interface de linha de comando.
-   Usando APIs.
-   Usando o PowerShell.
-   

## Perguntas:


1.

Qual tipo de expansão envolve adicionar ou remover recursos (como máquinas virtuais ou contêineres) para atender à demanda?

Dimensionamento vertical

Dimensionamento horizontal [x]
-> A escala horizontal é adição ou subtração do número de recursos.

Escala direta

2.

O que é caracterizado como a capacidade de um sistema de se recuperar de falhas e continuar funcionando?

Confiabilidade [x]
-> A escala horizontal é adição ou subtração do número de recursos.

Previsibilidade

Escalabilidade