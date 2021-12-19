# Elements & Components

React embraces the fact that rendering logic is coupled with other UI logic. It
combines those loosely in a unit called `component`.

React elements are 'descriptions' of what to be rendered on screen. React read
those and build DOM (Document Object Model). React elements are plain objects.

React elements are **immutable**. It represents the UI at a certain point in
time. Components are composed of React elements.

React DOM compares the node and its children with previous one and only update
what has changed.

Components are basically JavaScript functions which accept inputs called
`props`(properties) and return react elements.

When React sees user-defined component, it passes JSX attributes and children
to it as a single object known as `props`.

React treats lower case components as DOM tags.

Name props from the component's own point of view instead of the context the
component is rendered.

If a component is:

- used several times or
- complex enough on its own

it is better to extract the component out as a separate component. The
component must never change its input.

