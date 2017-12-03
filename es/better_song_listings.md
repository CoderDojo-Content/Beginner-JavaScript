1. Cualquiera que revise tu página de música se sentirá un poco confundido, querrá saber si estás enumerando canciones con el mismo título, o versiones grabadas por diferentes artistas. Por lo tanto, debes agregar más información a la lista de canciones. Específicamente, el nombre del artista. Cuando estás creando listas de canciones, estás utilizando la función _displaySongsList \(\)_. Ya escribí esa función y puedes encontrarla en el archivo "functions.js". Es algo como esto:

```javascript
   var wrapper = document.getElementById ('jsSpace')

   var songsListDisplay = document.createElement ('ul')

   var song = songsList[0]

   songsListDisplay.appendChild(buildSongDisplay(song))

   wrapper.appendChild(songsListDisplay)
 }
```

La versión que observas en el archivo tiene algunas **notas \(en verde\)** sobre lo que hace cada línea, pero la que es importante, en este momento, es esta:

```
    songsListDisplay.appendChild(buildSongDisplay(song))
```

1. Están sucediendo muchas cosas aquí, con funciones dentro de las funciones. Vale la pena que leas los comentarios en el archivo para entenderlo. Solo podía agregar un texto, pero quería usar un poco de HTML más sofisticado y agregar algunos valores de la canción, así que escribí otra función llamada _buildSongDisplay \(\)_. Está en la parte superior del archivo y  debería verse así:

```javascript
function buildSongDisplay (song) {
  var songDisplay = document.createElement ('li')
  var songInfo = '<strong>' + song.title + ' </strong> &#9658;'
  songDisplay.innerHTML = songInfo
  songDisplay.classList.add ('songListItem')
  songDisplay.dataset.songId = song.id
  return songDisplay
}
```

Las líneas importantes, para ti, son las que le dicen a la página qué elementos entran dentro de esa "li"

```javascript
songDisplay.innerHTML = songInfo
```

La primera línea crea una variable y almacena texto en ella, incluyendo `song.title`, que es una propiedad de la variable de la canción que pasa a la función. La segunda línea lo coloca dentro del `li`. Debes cambiar la segunda línea para agregar el artista. Primero, para agregar la palabra `by`, tendrá que cambiar esa primera línea como esta:

```javascript
var songInfo = '<strong>' + song.title + ' </strong> by &#9658;'
```

Ahora guarda el cambio y regresa a la página "music.html". Deja que vuelva a cargar y ve la diferencia. Puedes agregar cualquier texto que desees allí. El extraño conjunto de símbolos y números al final \(►\) te da la flecha de reproducción. Prueba con otros cuatro números y observa lo que obtienes. Sin embargo, ¡vuelve a cambiarlo después!

1. Regresa a "functions.js" y cambia la línea un poco más, para buscar la propiedad del artista de la canción, como esta:

```javascript
 var songInfo = '<strong>' + song.title + ' </strong> by '+ song.artist +'&#9658;'
```

Tenga en cuenta que debes dejar las comillas simples `(')` y usar un signo `+` a cada lado de la variable \(**las propiedades son un tipo particular de variable**\) nombre. Vuelve a cargar la página "music.html" y compruébalo.

Hay algunas propiedades más de la canción que puedes usar. Actualiza la función _buildSongDisplay \(\)_ para visualizar uno o dos más de ellos::

1. _género_: el tipo de música, p. pop, rock, dance, etc.

2. _Fecha de lanzamiento_: cuando se lanzó la canción.

3. _longitud_: cuánto dura la canción completa
   .

Si ya has hecho las Sushi Cards HTML para Principiantes, o conoces HTML de otra forma, ¡prueba algunas otras etiquetas aquí también! ¡Tal vez agregando una clase al &lt;strong&gt; y juega con el CSS!

¡Ahora revisa tus cambios en "music.html" otra vez!

