1. In these Sushi Cards you'll be learning JavaScript—one of the world's most popular programing languages. You probably use things built with it every day. It's in every major website, including YouTube, Facebook, Instagram and Google. It's also in lots of mobile apps and browser games.
2. Go to [dojo.soy/trinket](http://dojo.soy/trinket) and click "Sign Up For Your Free Account" if you do not already have an account. You will need an email address to sign up.
3. Enter your email address and choose a password, or ask somebody to do this for you.
4. Creating an account allows you to save your work and access it from any computer. It also allows you to make a copy of a project somebody else has shared with you so you can make your own changes to it!
5. Go to [dojo.soy/js-b-start](http://dojo.soy/js-b-start). You will see a box containing an example JavaScript website project. On the right hand side is the website, and on the left hand side is the code that makes the website.
    If you are not signed in, you will need to enter your email address and password to be able to **Remix** the project.
6. Click the "Remix" button at the top right of the project \(if it is not green, you have to sign in and then click it again\). This creates a copy of the project for you to work with. It should say "remixed" after you click it ![](/assets/remixedWide.png)
7. Next to the "Sign Out" button at the very top right corner of the page you should see your username and a drop-down menu \(the tiny triangle tells you there is a drop-down\). Click on it to show the menu and then select "My Trinkets". ![](/assets/MyTrinketsMenuWide.png)
    In Trinket \(this website\), projects are called "Trinkets"
8. The project you just remixed will be shown together with some example projects for other programing languages. It will be called "Beginner JavaScript Remix". Click on it to begin editing!
9. These cards are designed to follow on from the beginner HTML Sushi Cards, but don't worry if you haven't done those. There's not much HTML in these cards and it'll be explained when you see it. Either way, you'll be getting some music from the internet and setting up a player on the page so the user can pick which track they want to listen to. The first thing you'll need to do is look at your “music.html” file and see that it's pretty basic:

   ```html
   <html>
       <body>
           <div id="jsSpace"></div>
       </body>
   </html>
   ```

  All you have there is the basic HTML code for a page with a `div` \(division\) element with an `id` attribute where the `div` is called "jsSpace". What you need to do now is include a few JavaScript files on the page. You do that using the `script` tag with the `src` attribute set to the name of your file. You've got three JavaScript files:

  * **techie-functions**—Some of my code that you don't need to change, but feel free to take a look to understand how it's working
  * **functions.js**—Some of my code that you'll need to make some changes to over the course of these Sushi Cards
  * **my-script.js**—Where you'll be writing most of your code

  The order you add the `script` tags in is important because you need to load a piece of code before you can use it. You'll need to load them in the order listed above, like so:
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

10. If you look in the preview of the page, you'll see that there's actually nothing visible on it right now! You're going to use JavaScript to insert HTML into the page. Specifically, you'll need to:

  * Get some song information from the internet
  * Display the names of the songs
  * Create a music player (it'll be invisible, but you'll hear it just fine!)
  * Let the user choose which song to play on that player
  
  You'll start to do all of this on the next card.