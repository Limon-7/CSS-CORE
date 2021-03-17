## CSS-Animation

#### Transform:

CSS transforms allow you to move, rotate, scale, and skew elements.
**transform:translate(X,Y)|scale(X,Y)|rotate(Xdeg,Ydeg)|skew(Xdeg,Ydeg)|matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY())**

- translate(): moves an element from its current position.translete(500px,400px)
- scale(): increase or decrease an element. scale(5,2)
- rotate():rotate an element clockwise or anticlockwise. rotate(-25deg)
- skew():skew an element based on X or Y axis.skew(20deg,30deg)
- matrix():The matrix() method combines all the 2D transform methods into one.
  **matrix(2,20deg)**

**transfor:translate3d(X,Y,Z)|scale3d(X,Y,Z)|rotate3d(Xdeg,Ydeg,Zdeg)**

#### Transition:

CSS transitions allows you to change property values smoothly, over a given duration.

- transition-property:specify the css property the transition effect for.
- transition-dely:Specifies a delay (in seconds) for the transition effect.
- transition-duration: how many times to take completing the transition.
- transition-timinig-function:specify the speed of the transition.
- transition: shortend property of all 4 transition elements.
  **transition:transition-property | transition-duration |transition-timing-function | delay**
  - example: transition:all 500ms ease 1s

##### transition-timing-function:

- ease:satrt slowly>then fast>end slowly;//default:ease
- ease-in:start slowly
- ease-out:end slowly
- ease-in-out: start slowly and end slowly
- linear: start slowly and end slowly
- cubic-bazier(n,n,n,n): custom fuction.

## Animation

The animation property in CSS can be used to animate many other CSS properties such as color, background-color, height, or width. Each animation needs to be defined with the @keyframes.

- @keyframes:

```
@keyframes example{
    from{}
    to{}
}
```

here from = 0% and to=100%. keyFrames workat 0 to 100%

### Animation-sub-properties:

- animation-name:nameof the @keyframes name to animated.
- animation-duration: how much time to take complete the animation
- animation-timing-function: same as transition timeing function.
- animation-delay:1s: how many delay to takes to satrt an animation
- animation-direction: it has 4 properties.
  .1 animation-direction:normal; //default. forward
  .2 animation-direction:reverse; //backword
  .3 animation-direction:alternate; // forword then backword
  .4 animation-direction:alternate-reverse; // backword then forword
  **alternate or alternate-reverse work only when we declare animation-iteration-count property **
- animation-iteration-count: how many times an animation will run. infinite for lifetimes.
- animation-fill-mode: sets which values are applied before/after the animation.
  For example, you can set the last state of the animation to remain on screen, or you can set it to switch back to before when the animation began.
  **animation-fill-mode:forward|backword|none**
- animation-play-state:pause/play the animation.**animation-play-state:paused|running**
- animation:name|duration|timing-function|delay|direction|iteration|fill-mode|play-state
