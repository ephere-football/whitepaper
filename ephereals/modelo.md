---
description: 'Endereço oficial do contrato: 0xF48b4c5E2C7115Fb696b5401648D47E07a83194C'
---

# Modelo

Em Ephere, os jogadores são ativos digitais não fungíveis, transferíveis e escassos, armazenados em um contrato inteligente que usa o padrão ERC-721 (também conhecido como NFT) na rede [Binance Smart Chain](https://coinmarketcap.com/alexandria/article/what-is-binance-smart-chain).

Estes têm atributos físicos e mentais, habilidades futebolísticas treináveis que são limitadas pela genética e propriedades visuais distintas, algumas das quais podem ser alteradas pelo proprietário. Os jogadores ganham experiência jogando partidas e também podem ficar cansados, lesionados, envelhecer e retirar-se — _estão vivos._

{% hint style="info" %}
Contrato oficial: [0xF48b4c5E2C7115Fb696b5401648D47E07a83194C](https://bscscan.com/token/0xF48b4c5E2C7115Fb696b5401648D47E07a83194C) ([Código fonte](https://github.com/ephere-football/contracts/blob/master/contracts/EphereFootballerERC721.sol))
{% endhint %}

### Atributos e habilidades

Queremos que Ephere seja um jogo divertido onde as pessoas possam expressar sua criatividade, engenhosidade e pensamento estratégico para maximizar suas chances de sucesso. Para conseguir isso, precisamos de um sofisticado motor de simulação de partidas, com a capacidade de simular uma ampla gama de situações, o que requer uma representação complexa dos jogadores. É por isso que nossos jogadores têm um amplo conjunto de atributos que descrevem vários aspectos que os tornam únicos:&#x20;

{% embed url="https://gist.github.com/agurodriguez/7bfb9a0683f0b5e08baf36451e146c96#file-ephere-football-player-csv" %}

Os **atributos da camada 1** são definidos quando o jogador é criado e não podem ser alterados posteriormente. Os dados são gravados na blockchain e ninguém (nem nós) pode modificá-los. A grande maioria dos _limites_ mentais, físicos e técnicos dos jogadores, como a Determinação, a Resistência ou a Definição, são atributos da camada 1.

Os **atributos da camada 2** podem flutuar com base na atividade do jogo. As informações são gravadas nos servidores de Ephere. Idade, Energia e Experiência são alguns atributos da camada 2. Os atributos mentais, físicos e técnicos também são atributos da camada 2, o que significa que eles representam o limite de habilidade na camada 1 e o valor atual do atributo na camada 2. Portanto, você pode realizar ações no jogo para aumentar (ou diminuir) seu valor. Estes são alguns exemplos:&#x20;

* Quando você faz uma sessão de treinamento para melhorar a habilidade de Marca de um jogador de futebol, o valor do atributo da camada 2 aumentará um pouco, mas o valor do atributo da camada 1 permanecerá idêntico. Em outras palavras, o valor real da Marca aumentará ligeiramente, mas o valor máximo da habilidade Marca permanecerá igual. Evidentemente, o valor do atributo na camada 2 não pode ser maior que o valor na camada 1.

{% hint style="warning" %}
No futuro, usaremos uma blockchain de alto desempenho -- provavelmente criada por nós -- para armazenar os atributos da camada 2.
{% endhint %}

### OVR

O OVR é uma média ponderada de alguns atributos de um Epheral. Eles são categorizados em cinco níveis diferentes de acordo com esse valor:

| Categoria | OVR     |
| --------- | ------- |
| Tier 1    | 95 - 99 |
| Tier 2    | 90 - 94 |
| Tier 3    | 82 - 89 |
| Tier 4    | 76 - 81 |
| Tier 5    | 70 - 75 |

### Retiro

À medida que os jogadores envelhecem, seu desempenho diminui. Os usuários poderão retirar seus jogadores se assim o desejarem, deixando espaço para o nascimento de novos jogadores (lembre-se que os jogadores são escassos). Por isso, eles serão recompensados.

{% hint style="warning" %}
A retirada de um jogador implica a queima do token ERC721.
{% endhint %}
