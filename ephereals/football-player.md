---
description: 'Endereço oficial do contrato: 0xF48b4c5E2C7115Fb696b5401648D47E07a83194C'
---

# Modelo

Em Ephere, os jogadores são ativos digitais não fungíveis, transferíveis e escassos, armazenados em um contrato inteligente que usa o padrão ERC-721 (também conhecido como NFT) na rede [Binance Smart Chain](https://coinmarketcap.com/alexandria/article/what-is-binance-smart-chain).

Estes têm atributos físicos e mentais, habilidades futebolísticas treináveis que são limitadas pela genética e propriedades visuais distintas, algumas das quais podem ser alteradas pelo proprietário. Os jogadores ganham experiência jogando partidas e também podem ficar cansados, lesionados, envelhecer e retirar-se — _estão vivos._

{% hint style="info" %}
Contrato oficial: [0xF48b4c5E2C7115Fb696b5401648D47E07a83194C](https://bscscan.com/token/0xF48b4c5E2C7115Fb696b5401648D47E07a83194C) ([Source code](https://github.com/ephere-football/contracts/blob/master/contracts/EphereFootballerERC721.sol))
{% endhint %}

### Atributos y habilidades

Queremos que Ephere sea un juego divertido en el que las personas puedan expresar su creatividad, ingenio y pensamiento estratégico para maximizar sus posibilidades de éxito. Para lograr esto necesitamos un motor de simulación de partidos complejo con la capacidad de simular un gran rango de situaciones. Esto también amerita un modelo de datos de los jugadores que sea complejo. Por esto es que nuestros jugadores tienen un amplio conjunto de atributos que describen varios aspectos que los hacen únicos:

{% embed url="https://gist.github.com/agurodriguez/7bfb9a0683f0b5e08baf36451e146c96#file-ephere-football-player-csv" %}

Los **atributos de capa 1** se definen cuando se crea el jugador y no pueden ser cambiados posteriormente. Los datos están escritos en la blockchain y nadie (ni siquiera nosotros) puede modificarlos. La gran mayoría de límites mentales, físicos y técnicos de los jugadores como la Determinación, Stamina, o Definición son atributos de capa 1.

Los **atributos de capa 2** pueden sufrir fluctuaciones basadas en la actividad del juego. La información es escrita en los servidores de Ephere. Edad, Energía, Experiencia son algunos ejemplos de atributos de capa 2. Los atributos mentales físicos y técnicos también son atributos de capa 2, lo que significa que representan el límite de habilidad en la capa 1 y el valor actual del atributo en la capa 2. Esto significa que puedes realizar acciones en el juego para aumentar (o disminuir) su valor. Estos son algunos ejemplos:

* Cuando realizas una sesión de entrenamiento para mejorar la habilidad de Marca de un jugador de fútbol, el valor del atributo de capa 2 aumentará ligeramente, pero el valor del atributo de capa 1 permanecerá intacto. En otras palabras, el valor de Marca real aumentará ligeramente, pero el valor máximo de la habilidad de Marca será el mismo. Por supuesto, el valor del atributo en la capa 2 no puede ser mayor que el valor en la capa 1.

{% hint style="warning" %}
En el futuro usaremos una blockchain de alto rendimiento --probablemente creada por nosotros-- para almacenar atributos de capa 2.
{% endhint %}

### Retiro

A medida que los jugadores envejecen su rendimiento disminuye. Los usuarios podrán retirar a sus jugadores si así lo desean, dejando espacio para que nazcan nuevos jugadores (Recuerda que los jugadores escasean). Por hacerlo serán recompensados.

{% hint style="warning" %}
Retirar a un jugador implica quemar el token ERC721.
{% endhint %}
