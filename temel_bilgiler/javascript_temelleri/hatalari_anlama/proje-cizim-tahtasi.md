### Giriş

Bu projede, portgolyonuza koyabileceğiniz ve DOM manipülasyonu becerilerinizi geliştirecek oldukça iyi bir oyuncak oluşturacaksınız. Bir eskiz defteri ve manyetik çizim tahtasının tarayıcı versiyonunu inşa edeceksiniz.

Bu proje sizin için kolay _olmamalı_. Doğru JavaScript metodlarını ve kullanılacak CSS kodlarını bulabilmek için bolca Google'ı kullanacaksınız -aslında, amaç bu! Daha önce öğrendiğiniz araçlarla bu projeyi _yapabilirsiniz_ ve eğer ihtiyacınız olduğunu düşünüyorsanız daha değinmediğimiz bir çok konuyu internetten öğrenebileceğiniz çokça kaynak var. Size ilk adımlarda rehberlik edeceğiz fakat bunları uygulamak size kalmış.

Eğer gerçekten takılı kaldıysanız, sohbet odasına uğrayın. Oradaki biri size doğru yönü gösterecektir.

### Ödev

<div class="lesson-content__panel" markdown="1">
Don't forget to commit early & often! You can [reference the Commit Message lesson here](https://www.theodinproject.com/paths/foundations/courses/foundations/lessons/commit-messages)!

1.  [Follow the instructions atop Odin's Recipes project](https://www.theodinproject.com/paths/foundations/courses/foundations/lessons/recipes#setting-up-your-projects-github-repository) to set up a Git repository for this project.
2.  Create a webpage with a 16x16 grid of square divs.
    *   Create the divs using JavaScript. Don't try making them by hand with copy and pasting in your HTML file!
    *   It's best to put your grid squares inside another "container" div \(which can go directly in your HTML\).
    *   You need make the divs appear as a grid \(versus just one on each line\). This is a perfect opportunity to apply what you have learned about flexbox.
    *   Be careful with borders and margins, as they can adjust the size of the squares!
    *   "OMG, why isn't my grid being created???"
        *   Did you link your CSS stylesheet?
        *   Open your browser's developer tools.
        *   Check if there are any errors in the JavaScript console.
        *   Check your "elements" pane to see if the elements have actually shown up but are somehow hidden.
        *   Go willy-nilly and add  `console.log` statements in your JavaScript to see if it's actually being loaded.
3.  Set up a "hover" effect so that the grid divs change color when your mouse passes over them, leaving a \(pixelated\) trail through your grid like a pen would.
    *   Hint: "Hovering" is what happens when your mouse enters a div and ends when your mouse leaves it. You can set up event listeners for either of those events as a starting point.
    *   There are multiple ways to change the color of the divs, including:
        *   adding a new class to the div.
        *   changing the div's background color using JavaScript.
4.  Add a button to the top of the screen that will send the user a popup asking for the number of squares per side for the new grid. Once entered, the existing grid should be removed and a new grid should be generated _in the same total space as before_ \(e.g. 960px wide\) so that you've got a new sketch pad. **Tip**: Set the limit for the user input to a maximum of 100. A larger number of squares results in more computer resources being used, potentially causing delays, freezing, or crashing that we want to prevent.
    *   Research `button` tags in HTML and how you can make a JavaScript function run when one is clicked.
    *   Also check out `prompt`s.
    *   You should be able to enter `64` and have a brand new 64x64 grid pop up without changing the total amount of pixels used.
5.  Push your project to GitHub!

#### Extra Credit
Transform the behavior of a square when interacting with the mouse by introducing a series of modifications. 

1. Rather than a simple color change from black to white, each interaction should randomize the square's RGB value entirely. 
2. Additionally, implement a progressive darkening effect where each interaction adds 10% more black or color to the square. The objective is to achieve a completely black square only after ten interactions.

You can choose to do either one or both of these challenges, it's up to you.
</div>