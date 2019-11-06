# training-info

La API seleccionada para el training es: https://swapi.co.
Es una API que proporciona informacion relacionada a la saga de Star Wars.

Para no pegarle a la API todo el tiempo seria ideal implementar alguna forma de cacheo de la informacion de la API con Redis.

En la documentacion (https://swapi.co/documentation) podemos encontrar que:
Swapi has rate limiting to prevent malicious abuse (as if anyone would abuse Star Wars data!) and to make sure our service can handle a potentially large amount of traffic. Rate limiting is done via IP address and is currently limited to 10,000 API request per day. This is enough to request all the data on the website at least ten times over. There should be no reason for hitting the rate limit.

En https://swapi.co/about se puede ver lo siguiente:

Statistics
People: 87
Planets: 61
Films: 7
Species : 37
Vehicles: 39
Starships: 37

Cada una de esas entidades esta relacionada con un endpoint, y cada una de esas entidades presenta relaciones con algunas de las demas entidades.
Un esquema de como se observan estas relaciones puede verse en:
https://dbdiagram.io/d/5dc2f85aedf08a25543d99eb

Una de las opciones que se nos ocurrio desde el lado de negocio sería que el trainee sea como la empresa de videjouegos y los usuarios sean quienes están registrados en el videojuego. Existen juegos donde un usuario tener más de un personaje en una sola sesión, como por ejemplo los juegos tipo rpg.
