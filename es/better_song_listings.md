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

2. Están sucediendo muchas cosas aquí, con funciones dentro de las funciones. Vale la pena que leas los comentarios en el archivo para entenderlo. Solo podía agregar un texto, pero quería usar un poco de HTML más sofisticado y agregar algunos valores de la canción, así que escribí otra función llamada _buildSongDisplay \(\)_. Está en la parte superior del archivo y  debería verse así:

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

3. Regresa a "functions.js" y cambia la línea un poco más, para buscar la propiedad del artista de la canción, como esta:

```javascript
 var songInfo = '<strong>' + song.title + ' </strong> by '+ song.artist +'&#9658;'
```

Notice that you need to leave the single quotes \(`'`\) and use a plus either side of the **variable** \(**properties** are a particular kind of **variable**\) name.  
Re-load the “music.html” page again and check it out.

4. There are a few more **properties** on the song that you can use. Update the `buildSongDisplay()` **function** to display one or two more of them:

* _genre_—the kind of music e.g. pop, rock, dance, etc.
* _releaseDate_—when the song was released
* _length_—how long the full song is

If you've done the Beginner HTML Sushi Cards, or know HTML some other way, try some other tags in here too! Maybe add a class to the `<strong>` and play with the CSS!  
Now check out your changes in “music.html” again!



