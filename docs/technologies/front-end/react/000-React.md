# Authenticate and Authorize using OAuth2

## Status

Approved

## Context

There's the need of implementing a user facing application on the Web.

## Decision

Evaluate React

## Consequences

### Pro: 
* React establishes a stable uni-directional data flow which allows to build applications that have a good level of decoupling by construction.
* React is a well known technology nowadays and there's a big support in the comunity
* React is a UI library, not a framework and sometimes one might need to "assemble" several technologies to make it's app work.

### Cons:
* React forces you to use JSX, which might be a problem for developers used to the separation of concerns (HTML, CSS, JS)
* React focuses on one-way data flow, moving to the lowest shared component the handling of the state. This might be a limitation in case of different parts of the UI that are interested in the same state. This forces to use 3rd party technologies (Redux, RXJS).
* React evolves really fast, tries not to break things (in terms of backward compatibility), but forces the team to change often approach due to different solutions to solve the same problem (Redux, useEffect hooks, Classes vs Pure Functional components).