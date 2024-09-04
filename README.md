- Major features of React
    - JSX syntax allows dev to write HTML in JS code
- JSX
    - Javascript XML is an XML like syntax extension to ECMAScript (expressiveness of JS in HTML like template). For exmaple, instead of using "createElement" we can write JS directly inside of element.
- Component
    - Reusable piece of code that contain HTML elements. It can be a class that extends "React.Component" with "render()" or it can be defined as a function. Function based components are more common since hooks and state can used to do what a class can do.
- PureComponent
    - In class components, the components extending React.PureComponent instead of React.Component become the pure components. When props or state changes, PureComponent will do a shallow comparison on both props and state by invoking shouldComponentUpdate() lifecycle method.
    
    Note: React.memo() is a higher-order component.
- State
    - an object that holds info that may change over the lifetime of a component. Whenever the state changes, the component re-renders.
- Prop
    - Inputs to components. Used to pass custom data or trigger state changes
    const ChildComponent = (props) => {}
- State VS Props
    - State mananged by component. Can be updated by using "setState()". Changes to state re-render component
    - Props are passed to a child component. Are read-only.
- Key in prop
    - A special attribute you should include when mapping over arrays to render data. Key prop helps React identify which items have changed, are added, or are removed. Index not recommend because it can change. Don't generate randoms
- Virtual DOM
    - in-memory representation of Real DOM. It is kept in memory and synced with real DOM. It is a step between render function and displaying elements. That process is called reconciliation
- How Virtual Dom works?
    - When there are changes, the UI re-rendered in Virtual DOM -> Then the virtual and real calculate the difference -> Real DOM is updated with only the new changes.
- Shadow DOM VS Virtual DOM
    - The Shadow DOM is a browser technology designed primarily for scoping variables and CSS in web components. The Virtual DOM is a concept implemented by libraries in JavaScript on top of browser APIs.