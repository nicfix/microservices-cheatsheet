# Virtualize Long Lists

## Status

Approved

## Context

When working with React.

If your application renders long lists of data (hundreds or thousands of rows), we recommended using a technique known as “windowing”. This technique only renders a small subset of your rows at any given time, and can dramatically reduce the time it takes to re-render the components as well as the number of DOM nodes created.

[source Facebook](https://it.reactjs.org/docs/optimizing-performance.html#virtualize-long-lists)

## Decision

Virtualize long lists, aka use windowing

## Consequences

The windowing technique can be achieved by using some pre-built component or by building one in-house.

[react-window](https://react-window.now.sh/) and [react-virtualized](https://bvaughn.github.io/react-virtualized/) are popular windowing libraries. They provide several reusable components for displaying lists, grids, and tabular data. 
You can also create your own windowing component, [like Twitter did](https://medium.com/@paularmstrong/twitter-lite-and-high-performance-react-progressive-web-apps-at-scale-d28a00e780a3), if you want something more tailored to your application’s specific use case.

[source Facebook](https://it.reactjs.org/docs/optimizing-performance.html#virtualize-long-lists)
