1. El código JavaScript normalmente se va formando con funciones: es decir, conjuntos de instrucciones unidas con un nombre. Piensen en algo así como preparar una taza de té como una función, como una serie de pasos:

   * Consigue una pava o un recipiente para calentar.
   * Agrégale agua a la pava.
   * Hierve el agua. 
   * Encuentra una tetera para colocar el agua allí.
   * Coloca el saquito de té en la tetera.
   * Agrega el agua caliente en la tetera.
   * Espera...
   * Busca una taza.
   * Sirve una taza de té.


   ¡Son muchos pasos! ¡Es mucho más fácil enseñarle a alguien a preparar una taza de té una vez y luego pedirle que haga eso nuevamente en el futuro! Es lo mismo con JavaScript. Usamos funciones para hacer a veces cosas bastante complejas con comandos simples. Lo mejor es que no tienes que escribir la función para usarlo. Para empezar, usa algunos de los míos actualizando tu archivo my-script.js para que se vea así:

   ```javascript
    getSongs()

    whenSongsReadyDo(
      function(){
        var mySongs = getSongTitlesAndArtists()
        displaySongsList(mySongs)
        setupPlayer()
      }
    )
   ```

   Lo que sucede aquí es que su código le pide a Internet algunas canciones con _getSongs \(\)_. Luego verifica una vez más si las canciones han llegado con _whenSongsReadyDo \(\)_ y, una vez que llegan, ejecuta la función dentro de él, que es el resto del código del programa. Ese fragmento siguiente del código hace tres cosas:

   * Obtiene una lista de canciones y las almacena en un contenedor, el cual es una variable llamada _"mySongs"_.
   * Coloca la lista en _"mySongs"_ con una función \(_displaySongsList_\) que los muestra mediante una creación en HTML.
   * Crea un reproductor de música y lo configura para reaccionar a los clics sobre las canciones.

2. Ahora cambia al archivo index.html y obseva la vista previa. Podrás ver que aparece un título de canción allí "Ayer" y un botón de reproducción. Si haces clic en el botón, la canción se reproducirá. Genial ¿no?, pero esto no es de mucha utilidad por algunas razones. Vas a modificarlas en las próximas tarjetas   :

   * Primero, "Yesterday" es una de las canciones más grabadas de la historia y no hay forma de saber de quién es esta versión. 
   * Segundo solo muestra una canción, aunque existen muchas versiones de "Yesterday".
   * Tercero, es probable que quieras tener música más actualizada en tu página web, ¡así que tendrás que probar otra cosa!

   ¡Es hora de que mejores **mi función**!



