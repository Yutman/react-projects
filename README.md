#### Hooks in React are functions that let you "hook into" React state and lifecycle features from function components. 
#### They were introduced in React 16.8 to enable state and other React features without writing a class. 
#### The most commonly used hooks are useState for managing state, useEffect for side effects, and useContext for accessing the context API.
#### Hooks allow for cleaner and more concise function components, encourage reusable code, and make it easier to follow the flow of a component's logic.
#### Below are react projects based on the hooks I've learned and here I effectively apply them.

# useState
#### The useState hook in React allows you to add state to function components. 
#### To use it, import useState from React and call it inside your component. 
#### It returns an array with two elements: the current state value and a function that updates it. 
#### You can use useState anywhere within a function component but not inside loops, conditions, or nested functions. Initialize it with a default value. 
#### It's crucial for managing data that changes over time within your component.

1. Birthday Reminder

# useEffect and Conditional Rendering
#### The useEffect hook in React is used for side effects in function components. 
#### It can replace lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount in class components. 
#### You use it by calling useEffect() and passing a function where you place your side effect logic. 
#### The second argument is a dependency array; useEffect runs after every render by default, but with this array, you can control when it runs based on changes to specific values. 
#### It's used for data fetching, subscriptions, or manually changing the DOM.

2. Tours
3. Reviews
4. Questions
5. Menu
6. Tabs
7. Slider
8. Forms
9. Lorem Ipsum Generator
10. Color Shades Generator
11. Grocery Bud

# useRef
12. Navbar

# useContext
13. Modal And Sidebar
14. Stripe Submenus

# useReducer and useContext
15. Cart
React Router and useCallback
Cocktails
