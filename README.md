Premise: Swipe from left for loading the options/ settings menu for a page ( similar to mail app in iphone)

Solution:

1. Add the jquery.swipe.optionsmenu.js script to the page (This script is enhanced from the jquery.jsswipe.js http://www.ryanscherf.net/demos/swipe/)
2. Add the jquery.animate-enhanced.js script to the page for smooth animations.

In the script jquery.swipe.optionsmenu.js the touchmove function checks if the swipe is happening from the complete left end of the screen and the swipe interaction reaches the threshold value defined in the defaults. once the threshold is reached, the options menu animates from the left end.

function touchMove(event){
event.preventDefault();finalCoord.x=event.targetTouches[0].pageX;
finalCoord.y=event.targetTouches[0].pageY;
changeX=originalCoord.x- finalCoord.x;
if(changeX<(defaults.threshold.x*-1)&& originalCoord.x <= 10){defaults.swipeRight()}
}

