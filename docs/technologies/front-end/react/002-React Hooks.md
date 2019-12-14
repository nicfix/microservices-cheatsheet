# React Hooks

## Status

Proposed

## Context

When working with React.

One of the main problems of React is to re-use code between components at different levels of the dom tree.

The usual approach is to move the implementation to higher order components and then pass it through properties using techniques like ["render-props"](https://it.reactjs.org/docs/render-props.html) or ["higher-order-components"](https://it.reactjs.org/docs/higher-order-components.html)

In v16.8.0 React introduced Hooks as a way to solve this problem.


## Decision

Evaluate React Hooks

## Consequences

#### Pros:
* The code results more concise
* No explicit handling of `this.state` in classes. In general no need for classes components
* Hooks are backward compatible (no need to rewrite components that do not use Hooks)


#### Cons:
* Hooks result depends on the order of execution :(
* Hooks force to use function components, they are not supported by class based components.
* Hooks introduce implicit side effects and subscriptions to state and context that make components harder to test.

