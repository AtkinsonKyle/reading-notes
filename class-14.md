# Daily Reading 14
## What Google Learned About Teams
<hr>

### Things To Know
- ‘‘Teams are more effective when everyone is friends away from work. It turned out no one had really studied which of those were true.’’ -Abeer Dubey. I don't agree with this because at some point two or more friends will butt heads and the team can essentially lose its close adhesion. One of the rules of business is to never work with friends or family due to this reason. What do you think?
- Project Aristotle was organized to study hundreds of Google’s teams and figure out why some stumbled while others soared
- "Group norms" are the traditions, behavioral standards and unwritten rules that govern how we function when we gather
- Google’s data, from Project Aristotle, indicated that psychological safety, more than anything else, was critical to making a team work

### My Opinion 
- As long as everyone gets a chance to talk, the collective intelligence is relatively similar, and there are great "group norms"(no one stepping on each other's toes or trying to be a jerk.) a team can be succesful. Everyone needs to receive the same workload and no one slacks off, a team can be good to go. Adhesion doesn't matter, you don't have to be friends outside of work, but as long as everyone treats each other with respect a team can flow well.

<br>

## CSS Transforms, Transitions, and Animations
<hr>

### Properties to Know
- `transform` The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values
  - The `rotate` value provides the ability to rotate an element from 0 to 360 degrees
  - The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically
  - Using the `scale` value within the transform property allows you to change the appeared size of an element
  - It is possible to scale only the height or width of an element using the `scaleX` and `scaleY` values
  - Using the `translateX` value will change the position of an element on the horizontal axis while using the `translateY` value will change the position of an element on the vertical axis
  - The distance values used within the `translate` value may be any general length measurement, most commonly pixels or percentages
  - `Skew` is used to distort elements on the horizontal axis, vertical axis, or both
  - The default transform origin is the dead center of an element, both 50% horizontally and 50% vertically. To change this default origin position the `transform-origin` property may be used. Can accept one or two values
  - In order for three-dimensional transforms to work the elements need a `perspective` from which to transform. Perspective is a value of transform, can be set as none.
  - `perspective-origin`
- 3D Rotate utilizes three new transform values, including `rotateX`, `rotateY`, and `rotateZ`
  - By using the `scaleZ` three-dimensional transform elements may be scaled on the z axis
  - `translateZ` value. A negative value here will push an element further away on the z axis, resulting in a smaller element. Using a positive value will pull an element closer on the z axis, resulting in a larger element
  - The `transform-style` property needs to be placed on the parent element, above any nested transforms. The `preserve-3d` value allows the transformed children elements to appear in their own three-dimensional plane while the flat value forces the transformed children elements to lie flat on the two-dimensional plane
- There are four transition related properties in total, including `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`
  - The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes
  - The `transition-property` property determines exactly what properties will be altered in conjunction with the other transitional properties
  - *** Not all properties may be transitioned ***, only properties that have an identifiable halfway point
  - The duration in which a transition takes place is set using the `transition-duration` property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms)
  - The `transition-timing-function` property is used to set the speed in which a transition will move. Keyword values for the `transition-timing-function` property include `linear`, `ease-in`, `ease-out`, and `ease-in-out`
    - The `linear` keyword value identifies a transition moving in a constant speed from one state to another. The `ease-in` value identifies a transition that starts slowly and speeds up throughout the transition, while the `ease-out` value identifies a transition that starts quickly and slows down throughout the transition. The `ease-in-out` value identifies a transition that starts slowly, speeds up in the middle, then slows down again before ending
  - The `transition-delay property` sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing
- To set multiple points at which an element should undergo a transition, use the `@keyframes` rule. The `@keyframes` rule includes the animation name, any animation breakpoints, and the properties intended to be animated
  - The `animation-name` declaration is applied to the element in which the animation is to be applied to. You also need to declare an `animation-duration` property and value so that the browser knows how long an animation should take to complete. A timing function and delay can be declared using the `animation-timing-function` and `animation-delay` properties respectively
    - To have an animation repeat itself numerous times the `animation-iteration-count` property may be used. Values for the `animation-iteration-count` property include either an integer or the infinite keyword. Using an integer will repeat the animation as many times as specified, while the infinite keyword will repeat the animation indefinitely in a never ending fashion
    - You may also declare the direction an animation completes using the `animation-direction` property. Values for the `animation-direction` property include `normal`, `reverse`, `alternate`, and `alternate-reverse`
      - The `normal` value plays an animation as intended from beginning to end. The `reverse` value will play the animation exactly opposite as identified within the @keyframes rule, thus starting at 100% and working backwards to 0%
      - The `alternate` value will play an animation forwards then backwards. Within the keyframes that includes running forward from 0% to 100% and then backwards from 100% to 0%. Using the `animation-iteration-count` property may limit the number of times an animation runs both forwards and backwards.
      - The `animation-fill-mode` property identifies how an element should be styled either before, after, or before and after an animation is run. The `animation-fill-mode` property accepts four keyword values, including `none`, `forwards`, `backwards`, and `both`
        - The `none` value will not apply any styles to an element before or after an animation has been run
        - The `forwards` value will keep the styles declared within the last specified keyframe
        - The `backwards` value will apply the styles within the first specified keyframe as soon as being identified, before the animation has been run
        - The `both` value will apply the behaviors from both the forwards and backwards values.
- fade, color, grow and shrink, rotate elements, square to circle, 3D Shadow, swing, inset border

```

.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}

```
```

  .rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}

```
```

.color:hover
{
        background:#53a7ea;
}

```

.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}

```
```

.shrink:hover
{
        -webkit-transform: scale(0.8);
        -ms-transform: scale(0.8);
        transform: scale(0.8);
}

```
```

.circle:hover
{
        border-radius:50%;
}

```

.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}

```

SET THE SWING

@-webkit-keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
       transform: translateX(-5px);
    } 
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}
@keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
        transform: translateX(-5px);
    }
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}

APPLY SWING

.swing:hover
{
        -webkit-animation: swing 1s ease;
        animation: swing 1s ease;
        -webkit-animation-iteration-count: 1;
        animation-iteration-count: 1;
}

```
```

.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}

```

