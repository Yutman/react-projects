#### Hooks in React are functions that let you "hook into" React state and lifecycle features from function components. 
#### They were introduced in React 16.8 to enable state and other React features without writing a class. 
#### The most commonly used hooks are useState for managing state, useEffect for side effects, and useContext for accessing the context API.
#### Hooks allow for cleaner and more concise function components, encourage reusable code, and make it easier to follow the flow of a component's logic.

# useState
#### The useState hook in React allows you to add state to function components. 
#### To use it, import useState from React and call it inside your component. 
#### It returns an array with two elements: the current state value and a function that updates it. 
#### You can use useState anywhere within a function component but not inside loops, conditions, or nested functions. Initialize it with a default value. 
#### It's crucial for managing data that changes over time within your component.

#### Project:
00. Birthday Reminder

# useEffect and Conditional Rendering
#### The useEffect hook in React is used for side effects in function components. 
#### It can replace lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount in class components. 
#### You use it by calling useEffect() and passing a function where you place your side effect logic. 
#### The second argument is a dependency array; useEffect runs after every render by default, but with this array, you can control when it runs based on changes to specific values. 
#### A cleanup return function is necessary when your effect sets up a subscription, listener, or any side effects that should be cleaned up to prevent memory leaks and performance issues.
#### This cleanup function is returned at the end of useEffect to remove those side effects when the component unmounts or before the effect runs again.
#### async/await
#### async/await is a syntax in JS that allows one to write asynchronous code that looks and behaves a bit more like synchronous code. This makes your asynchronous code easier to write, read, and debug. It is used in React with this hook mainly for data fetching.
#### Below is an example derived from one of the tutorials:
 const getUsers = async () => {
    const response = await fetch(url);
    const users = await response.json();
    setUsers(users);
    // console.log(users);
  };

  useEffect(() => {
    getUsers();
  }, []);
#### I can best describe the example as; 'getUsers' is an asynchronous function fetching users from a URL using fetch. The await keywords pause execution until the fetch request and conversion to JSON complete, ensuring setUsers is called with the fetched data. The function is called inside a useEffect with an empty dependency array, meaning it runs once when the component mounts, similar to componentDidMount in class components. This pattern is common for initializing component state with data from an API.

#### It's used for data fetching, subscriptions, or manually changing the DOM.

#### Projects: 
01. Tours
02. Reviews
03. Questions
04. Menu
05. Tabs
06. Slider
07. Sidebar

# Forms
08. Lorem Ipsum Generator
09. Color Shades Generator
10. Grocery Bud

# useRef
#### The useRef Hook allows you to persist values between renders.
#### It can be used to store a mutable value that does not cause a re-render when updated. This is because changing the current property of the useRef object doesn't trigger a re-render
#### It can be used to access a DOM element directly within functional components. This is useful for tasks like focusing an input field, measuring an element's dimensions, or triggering imperative DOM operations.
#### For example, we can we can access and manipulate DOM elements directly without needing to use traditional DOM manipulation methods like document.getElementById().
#### The useRef Hook can also be used to keep track of previous state values. This is because we are able to persist useRef values between renders.

11. Navbar

# useContext
12. Modal And Sidebar
13. Stripe Submenus

# useReducer and useContext
#### useReducer is a hook in React that is used for managing complex state logic in your components.
#### It is an alternative to useState that is more suitable for managing state in scenarios where the state logic is complex or involves multiple sub-values, or when the next state depends on the previous one.
#### useReducer can help to avoid duplicating state logic across multiple useState calls by encapsulating the logic within the reducer function.
#### const [state, dispatch] = useReducer(reducer, initialState) accepts 2 arguments: the reducer function and the initial state. Also, the reducer returns an array of 2 items: the current state and the dispatch function.
#### To update the state call dispatch(action) with the appropriate action object. The action object is then forwarded to the reducer() function that updates the state. If the state has been updated by the reducer, then the component re-renders, and [state, ...] = useReducer(...) hook returns the new state value.

14. Cart
15. React Router and useCallback
16. Cocktails


NB: To resolve ERR_OSSL_EVP_UNSUPPORTED error, which is triggered by changes in OpenSSL 3.0 used by Node.js I used the following command in my terminal:
```
$env:NODE_OPTIONS="--openssl-legacy-provider" 
npm start
```
