## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

### How to run
You can run original site by http://dalex01.github.io/frontend-nanodegree-mobile-portfolio/
You can run original site by http://dalex01.github.io/frontend-nanodegree-mobile-portfolio/build/

### Changes was made in pizza website
1. Move all variables declarations which are not changed during the loop out of the for-loops. See lines 447-453, 467-470, 502-528 of main.js
2. Reduce the number of pizzas painted in .mover class. See lines 549-558 of main.js
3. Change all querySelectorAll by getElementsByClassName as the last one is faster.
4. Create array pizzaItems with all items with class name .mover during thier creation and use this array in updatePostion function. We remove one more access to DOM by creation of this array beforehand.
5. Update for-loop in updatePostion function to remove using "%" (monulo) in the loop. Now loop is designed to calculate all five phases at a time.
6. Update sizeSwitcher function to return percent during changing size of pizza.
7. Added the following properties to .mover class in style.css:
** will-change: transform;
** transform: translateZ(0);
** transform: translate3d(0,0,0);
** -webkit-backface-visibility: hidden;
 

P.S. It is a time killer project :) I'm not sure that I mention here all changes during my investigation.