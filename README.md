# Qué hace meneaRme
MeneaRme es un web scraper en R para el agregador de enlaces meneame.net. Proporcionándole unos pocos argumentos devolverá un csv con los siguientes campos:

- Fecha
- Titular
- Entradilla
- Meneos
- Clics
- Comentarios
- Votos positivos
- Votos negativos
- Votos anónimos
- Karma
- Comentarios
- Nombre del usuario que ha compartido el contenido
- Web de origen
- El sub del que forma parte el contenido 
- El link al contenido


# Instalación 

Para instalarlo es tan fácil como ejecutar el comando ```devtools::install_github("meneos/meneaRme)```.

# Cómo funciona

MeneaRme tiene tres funciones: una para scrapear la portada (```portada()```), otra para los subs (```submeneame()```) y otra para scrapear búsquedas por palabras (```busca()```).

# Ejemplos de uso

## portada()
El comando ```portada(paginas = 10)``` scrapea las diez primeras páginas de la [Edición General](https://www.meneame.net/).

## submeneame()
El comando ```submeneame(sub = "Series", paginas = 10)``` scrapea las diez primeras páginas del sub [Series](https://www.meneame.net/m/Series).

## busca()
El comando ```busca(palabra = "guerra siria", paginas = 10)``` scrapea las diez primeras páginas de la búsqueda "guerra siria" en el buscador de meneame.net. Es importante señalar que para las búsquedas meneame solo ofrece 40 páginas por lo que el argumento paginas solo aceptará números por debajo del 41. Para conseguir el máximo número de entradas meneaRme scrapea los resultados de búsquedas por relevancia y por fecha. Esto significa que probablemente el csv resultante contendrá duplicados que habrá que limpiar posteriormente.


