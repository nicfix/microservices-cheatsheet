# React Hooks

## Status

Proposed

## Context

When working with React.

One of the main problems of React is to re-use code between components at different levels of the dom tree.

The usual approach is to move the implementation to higher order components and then pass it through properties using techniques like ["render-props"](https://it.reactjs.org/docs/render-props.html) or ["higher-order-components"](https://it.reactjs.org/docs/higher-order-components.html)

In v16.8.0 React introduced Hooks as a way to solve this problem.


## Decision

Evaluate [React Hooks](https://reactjs.org/docs/hooks-intro.html)

## Consequences

#### Pros:
* The code results more concise
* No explicit handling of `this.state` in classes. In general no need for classes components
* Hooks are backward compatible (no need to rewrite components that do not use Hooks)


#### Cons:
* Hooks result depends on the order of execution :(
* Hooks force to use function components, they are not supported by class based components.
* Hooks introduce implicit side effects due to subscriptions to state and context changes. This can make components harder to test.


### Controverse quotes
Regarding useEffect https://it.reactjs.org/docs/hooks-reference.html#useeffect

> Instead, use useEffect. The function passed to useEffect will run after the render is committed to the screen. Think of effects as an escape hatch from React’s purely functional world into the imperative world.

