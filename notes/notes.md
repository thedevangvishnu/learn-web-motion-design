# MOTION DESIGN FOR WEB

## The basics

- What is motion design?

  - It's a creative discipline that brings static elements to life by adding motion.
  - Motion design can be achieved by the use of videos, transitions and animations that can covert a simple static element into a much-interesting, visually appealing, informative moving element.

- Trinity:

  - Videos

    - These are one of the best tools to add motion. They are a blend of visuals, text, motion and story.
    - Videos are worth a thousand pictures.

  - Transitions

    - Transitions allow for a smooth change in properties of an element from state A to state B.
    - Can be done create simple and swift change in motion.

  - Animation
    - Similar to transitions but are more complex and can give more complex and better results
    - Used for more continuous transitions to create a "flowing-motion"

- Significance

  - Informative
    - Adding motion to elements can allow user to draw attention, thus informing them about the element.
  - Aesthetic
    - Adding motion to elements also adds to the stylistic aspect and add up to the personality and whole vibe of a website/element.

## CSS Transiitons

- These are a functionality provided by CSS that allow smooth and gradual change in element's properties over a specified duration.
- There's no point of reference or stop between those two points when applying transitions. It's simple: Point A --> transitions to --> Point B
- The four main properties for transition in CSS:

  - transition-property: other css property name on which transition effect must be applied
  - transition-duration: duration for which the transition effect should be applied
  - transition-timing-function: patterns for transition to kick-in and go-out
  - transiiton-delay: time after which the transition effect should get applied

  - shorthand property: "transition"

- To create overlay transitions

  - we use background: linear-gradient(), but transition-property doesn't apply on background or background-image properties.
  - for that, we can add a ::before element (or use other pseudo elements) and give background: linear-gradient() to it. Then, we can add transition to this ::before element on main-element:hover
  - slick designs can be achieved using just transition, transform and opacity property

- Transitions are not only applied on hovers. They can also be applied if an extra class is added or removed

## CSS Animations

- CSS animation is way to make elements gradually change their position or appearance over time.
- It is done by defining "keyframes", which are points of in-between states of this change.
- Animation is thus crated, by smooth transitioning between these keyframes.

- How to create animations in CSS?

  - The important thing is to define an amination by creating keyframes
  - Then apply the created animation to an element using "animation" property
  - animation: duration | easing-function | delay | iteration-count | direction | fill-mode | play-state | name;
    - The order is important

- Difference between animations and transitions
  - animations have keyframes (in-between states of the change) while transiitons don't
  - animations can be "iteration" (meaning can be ran once or more) while transiitons run only once
  - animations have "direction" (which way the animation should run: forward, backward, alternate, etc.) while transitions run only forward
  - animations have "play-state" (that is they can be paused in between their execution) while transitions must end once ran.

```
// CSS styles sheet

@keyframes animationName {
  from {
    // initial values for any css propertyies
  }
  to {
    // final value for that same css properties
  }
}


```

- Example

```
// CSS styles sheet

.box {
  animation: 2s ease-in-out 1s 2 moveRight;
}


@keyframe moveRight {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(100px);
  }
}
```
