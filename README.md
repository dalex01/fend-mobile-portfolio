# Website Performance Optimization portfolio project

I optimized provided online portfolio for speed! In particular, the critical rendering path was optimized and this page render was made as quickly as possible by applying the techniques I had picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

## Requirements

Project was reviewed according to this [rubric](http://i.imgur.com/fblSMf8.png).

# How to use

* To see this project on your PC you should just clone repository with command `git clone https://github.com/dalex01/fend-mobile-portfolio.git` and start index.html file.
* Or [click](http://dalex01.github.io/fend-mobile-portfolio)

## Changes was made in pizza website

1. Move all variables declarations which are not changed during the loop out of the for-loops. See lines 447-453, 467-470, 502-528 of main.js
2. Reduce the number of pizzas painted in .mover class. See lines 549-558 of main.js
3. Change all querySelectorAll by getElementsByClassName as the last one is faster.
4. Create array pizzaItems with all items with class name .mover during thier creation and use this array in updatePostion function. We remove one more access to DOM by creation of this array beforehand.
5. Update for-loop in updatePostion function to remove using "%" (monulo) in the loop. Now loop is designed to calculate all five phases at a time.
6. Update sizeSwitcher function to return percent during changing size of pizza.
7. Added the following properties to .mover class in style.css:
  - will-change: transform;
  - transform: translateZ(0);
  - transform: translate3d(0,0,0);
  - -webkit-backface-visibility: hidden;

P.S. It is a time killer project :) I'm not sure that I mention here all changes during my investigation.