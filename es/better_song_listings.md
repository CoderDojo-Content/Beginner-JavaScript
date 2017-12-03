1. Cualquiera que revise tu página de música se sentirá un poco confundido, querrá saber si estás enumerando canciones con el mismo título, o versiones grabadas por diferentes artistas. Por lo tanto, debes agregar más información a la lista de canciones. Específicamente, el nombre del artista. Cuando estás creando listas de canciones, estás utilizando la función _displaySongsList \(\)_. Ya escribí esa función y puedes encontrarla en el archivo "functions.js". Es algo como esto:

   ```javascript
    function displaySongsList (songsList) {

      var wrapper = document.getElementById ('jsSpace')

      var songsListDisplay = document.createElement ('ul')

      var song = songsList[0]

      songsListDisplay.appendChild(buildSongDisplay(song))

      wrapper.appendChild(songsListDisplay)
    }
   ```

   La versión que observas en el archivo tiene algunas **notas \(en verde\)** sobre lo que hace cada línea, pero la que es importante, en este momento, es esta: 

2. songsListDisplay.appendChild\(buildSongDisplay\(song\)\)

3. There's a lot happening here, with **functions** inside **functions**. The **comments** in the file are worth reading to understand it.I could just append a piece of text, but I wanted to use some fancier HTML and add some values from the song, so I wrote another **function** called `buildSongDisplay()`. It's at the very top of the file and right now just looks like this:

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

   The important lines, for you, are the ones that tell the page what goes inside that `li`.

   ```javascript
   var songInfo = '<strong>' + song.title + ' </strong> &#9658;'
   songDisplay.innerHTML = songInfo
   ```

   The first line creates a variable and stores text in it, including `song.title`, which is a **property** of the `song` **variable** that gets **passed** into the **function**. The second line puts it inside the `li`. You want to change the second line to add the artist. First, to add the word “by”, you'll need to change that first line like this:

   ```javascript
   var songInfo = '<strong>' + song.title + ' </strong> by &#9658;'
   ```

   Now save the change and go back to the “music.html” page. Let it reload and see the difference. You can add any text you like in there. The weird set of symbols and numbers at the end \(`&#9658;`\) gives you the play arrow. Try another four numbers and see what you get. Change it back afterwards though!

4. Go back to “functions.js” and change the line a little more, to look up the artist **property** of the song, like this:

   ```javascript
    var songInfo = '<strong>' + song.title + ' </strong> by '+ song.artist +'&#9658;'
   ```

   Notice that you need to leave the single quotes \(`'`\) and use a plus either side of the **variable** \(**properties** are a particular kind of **variable**\) name.  
   Re-load the “music.html” page again and check it out.

5. There are a few more **properties** on the song that you can use. Update the `buildSongDisplay()` **function** to display one or two more of them:

   * _genre_—the kind of music e.g. pop, rock, dance, etc.
   * _releaseDate_—when the song was released
   * _length_—how long the full song is

   If you've done the Beginner HTML Sushi Cards, or know HTML some other way, try some other tags in here too! Maybe add a class to the `<strong>` and play with the CSS!  
   Now check out your changes in “music.html” again!



