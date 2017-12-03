1. En estas Sushi Cards, aprenderás JavaScript, uno de los lenguajes de programación más populares del mundo. Probablemente uses cosas construidas con esto todos los días. Está en todos los sitios web importantes, incluidos YouTube, Facebook, Instagram y Google. También está en muchas aplicaciones móviles y juegos del navegador.
2. Ve a dojo.soy/trinket y haz clic en "Registrarse en tu cuenta gratuita" si aún no tienes una cuenta. Necesitarás una dirección de correo electrónico para registrarte.
3. Ingresa tu dirección de correo electrónico y elije una contraseña, o solicita a alguien que lo haga por ti.
4. Crear una cuenta te permite guardar tu trabajo y acceder a él desde cualquier computadora. ¡También te permite hacer una copia de un proyecto que otra persona ha compartido contigo para que puedas hacer tus propios cambios!
5. Ve a dojo.soy/js-b-start. Verás un cuadro que contiene un ejemplo de proyecto de un sitio web de JavaScript. En el lado derecho está el sitio web, y en el lado izquierdo está el código que construye el sitio web.
   Si no has iniciado sesión, deberás ingresar tu dirección de correo electrónico y contraseña para poder **remixarlo** el proyecto.
6. Haz clic en el botón "Remix" en la parte superior derecha del proyecto \(si no está  en verde, debes iniciar sesión y luego hacer clic de nuevo\). Esto crea una copia del proyecto para que puedas trabajar. Debería decir "remezclado" después de hacer clic sobre él.
7. Al lado del botón "Cerrar sesión" en la esquina superior derecha de la página, deberías ver tu nombre de usuario y un menú desplegable \(el pequeño triángulo indica que hay un menú desplegable\). Haz clic en él para mostrar el menú y luego selecciona "My Trinkets". Ten en cuenta que en Trinket los proyectos se llaman "Trinkets".
8. El proyecto que acabas de remezclar se mostrará junto con otros proyectos de ejemplo para otros lenguajes de programación. Se llamará "Beginner JavaScript Remix". ¡Haz clic sobre él para comenzar a editar!
9. Estas tarjetas están diseñadas para ser la continuación de las tarjetas Sushi HTML para principiantes, pero no te preocupes si no las has hecho. No hay mucho HTML en estas tarjetas y se explicará cuando lo veas. De cualquier manera, recibirás música de Internet y configurarás un reproductor en la página para que un usuario pueda elegir qué pista quiere escuchar. Lo primero que debes hacer es mirar tu archivo "music.html" y ver que es bastante básico:

   ```html
   <html>
       <body>
           <div id="jsSpace"></div>
       </body>
   </html>
   ```

   Todo lo que tienes allí es el código HTML básico para una página, con un elemento **div** \(división\) con un atributo** id** donde el div se llama _"jsSpace"_. Lo que debes hacer ahora es incluir algunos archivos JavaScript en la página. Lo haces utilizando la etiqueta de** script** con el atributo **src** relacionado con el nombre de su archivo. Tienes entonces tres archivos JavaScript:

   * **techie-functions**—Parte del código que no necesitas cambiar, pero no dudes en observarlo para comprender cómo funciona     .
   * **functions.js**—Parte del código que necesitará hacer algunos cambios en el transcurso de estas Sushi Cards.
   * **my-script.js**—Donde escribirás la mayor parte del código.

   El orden en el que agregas las etiquetas de secuencia de comandos es importante porque necesitas cargar un fragmento de código antes de poder usarlo. Deberás cargarlos en el orden indicado anteriormente, de esta forma:

   ```html
   <html>
       <body>
           <div id="jsSpace"></div>
           <script src="techie-functions.js"></script>
           <script src="functions.js"></script>
           <script src="my-script.js"></script>
       </body>
   </html>
   ```

10. Si observas la vista previa de la página, ¡verás que en realidad no hay nada visible en ella ahora mismo!     Para ello vas a usar JavaScript para insertar HTML en la página. Específicamente, necesitarás:

    * Obtener información de alguna canción en Internet.
    * Mostrar los nombres de las canciones.
    * Crear un reproductor de música \(¡será invisible, pero lo escucharás bien!\)
    * Permitir que un usuario elija qué canción escuchar en ese reproductor      .

    Comenzarás a hacer todo esto en la próxima carta!



