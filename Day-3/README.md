# Week-5 -- Day-3

## It's Game Day!

Let's develop a game! There is a catch, you will only have one to two weeks to develop it and you can only use JavaScript, HTML, CSS (Bootstrap). Here are some visual examples of games you can create:

![super hero memory game](https://camo.githubusercontent.com/c59c2abeb2ede6af38e6ea58f2f66039ea8d0595/68747470733a2f2f692e696d6775722e636f6d2f4836474c5a47512e6a7067)

![Blackjack Game](https://github.com/RyanPGeorge/project1-blackjack/blob/master/screenshots/blackjack-sc3.png?raw=true)

![Minesweeper](https://github.com/christopherallanperry/WDI_PROJECT_1/raw/master/docs/project_01_winning_game.png)

## Recommended Developing Process

 1. Setup your Folder Structure
 2. Create Basic Grid
 3. Carefully Buildup JavaScript
 4. Finish Design

### Setup you Folder Structure

For the sake of this tutorial / notes let's build a simple tic tac toe game.
But before you can start coding start set up your folder structure for this project.
Create a root directory with an appropriate name. Then create "css", "js" folders inside of it and finally create index.html file.

    - tic_tac_toe_game
    	- css
    		- styling.css
    	- js
    		- script.js
    	- index.html

### Create Basic Grid (Using Bootstrap)

Here is how you can create a basic 3x3 grid using bootstrap. It's pretty simple

    <div class="container">
          <div class="row">
            <div class="col-md-4"></div>
            <div class="col-md-4"></div>
            <div class="col-md-4"></div>
          </div>
          <div class="row">
            <div class="col-md-4"></div>
            <div class="col-md-4"></div>
            <div class="col-md-4"></div>
          </div>
          <div class="row">
            <div class="col-md-4"></div>
            <div class="col-md-4"></div>
            <div class="col-md-4"></div>
          </div>
      </div>


Don't forget to load bootstrap!

You are not going to see anything yet. You stil need to add a border, content to each cell and maybe adjust the height of the cells. To do some of those things you will need to add extra class names.

    <div class="container board">
      <div class="row">
        <div data-cell="1" class="col-md-4 board-cell"></div>
        <div data-cell="2" class="col-md-4 board-cell"></div>
        <div data-cell="3" class="col-md-4 board-cell"></div>
      </div>
      <div class="row">
        <div data-cell="4" class="col-md-4 board-cell"></div>
        <div data-cell="5" class="col-md-4 board-cell"></div>
        <div data-cell="6" class="col-md-4 board-cell"></div>
      </div>
      <div class="row">
        <div data-cell="7" class="col-md-4 board-cell"></div>
        <div data-cell="8" class="col-md-4 board-cell"></div>
        <div data-cell="9" class="col-md-4 board-cell"></div>
      </div>
    </div>

See how I added `board` `board-cell` classes. You can ignore the `data-cell` attribute for now.

Here is some styling you can add in order to view something on the a page.

     * {
       border-style: dotted;
       border-width: thin;
     }

    .board-cell {
      height: 200px;
      font-size: 100px;
      text-align: center;
    }

    .board {
      margin-top: 2em;
    }


You should see something like this on the page:

![simplest game board](https://raw.githubusercontent.com/Team-FCB/Assets/master/game_board.png)

### Add some Flavor (JavsScript)

Ready for your first (maybe not) JavaScript in a Browser? Here we go. Let's make each cell clickable. The good news we already attached a new class `board-cell`  to each cell. We can use that class name to attach an event listener! You ask what is an event listener? Well, as the name suggests it waits for an event (click, hover etc.) and then fires up some JavaScript. Let's add a click event listener to each cell. Here is one way to do it. There are at least three different ways to do this very same thing. One involves jQuery. But back to this event listener.

    document.querySelectorAll('.board-cell').forEach(item => {
      item.addEventListener('click', event => {
        let element = event.target;
        // Do some action. In this case alert a statement
        alert("Got it.")
	  })
    });

Now when somebody clicks on a cell it alerts the message "Got it."

I am not going to go over the remaining part of the JavaScript, at least not yet.

### Finish Design

I think once you have the functionality aspect down and the app is functioning you can focu on design. Personally, that is my preference. You do not have to do it in this order but I like knowing that I completed the hard part of the assignment first and any remaining time can now be spend in making it look good.
