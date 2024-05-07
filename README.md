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
# Prop Drilling
#### In React, "props" is short for "properties". Props are a way to pass data from parent components to child components.
#### They are immutable (read-only) and are used to customize and configure child components.
#### Prop drilling is the process of passing data (props) from a higher-level component to a lower-level component through intermediary components that don't directly use the data themselves.
#### Modern React development often favors other state management solutions over prop drilling in certain scenarios. 
#### Why? 
#### 1.  Prop drilling can lead to increased complexity
#### 2.  Prop drilling can lead to performance issues due to unnecessary re-renders triggered by changes in props at higher levels of the hierarchy
#### 3. Modifying the data flow may require updates to multiple components, increasing the risk of introducing bugs and making maintenance more time-consuming.
#### 4. The React Context API, combined with hooks like useContext, provides a way to share state across multiple components without the need for prop drilling. 
#### The useContext hook is based on Context API and works on the mechanism of Provider and Consumer. Provider needs to wrap components inside Provider Components in which data have to be consumed. Then in those components, using the useContext hook that data needs to be consumed.


12. Modal And Sidebar
13. Stripe Submenus

# useReducer and useContext
#### useReducer is a hook in React that is used for managing complex state logic in your components.
#### It is an alternative to useState that is more suitable for managing state in scenarios where the state logic is complex or involves multiple sub-values, or when the next state depends on the previous one.
#### useReducer can help to avoid duplicating state logic across multiple useState calls by encapsulating the logic within the reducer function.
#### const [state, dispatch] = useReducer(reducer, initialState) accepts 2 arguments: the reducer function and the initial state. Also, the reducer returns an array of 2 items: the current state and the dispatch function.
#### To update the state call dispatch(action) with the appropriate action object. The action object is then forwarded to the reducer() function that updates the state. If the state has been updated by the reducer, then the component re-renders, and [state, ...] = useReducer(...) hook returns the new state value.

# React Router
####  Routing refers to the process of determining which UI component should be displayed to the user based on the current URL or location within the application.
#### Create-React-App doesn't include page routing.
#### A separate library named React Router enables routing in React applications and allows defining multiple routes in an application.

### React Router vs. React Router DOM: the Difference
#### react-router is the core package containing standard components and functionalities to implement routing in React applications.
#### react-router-dom is a specialized package that you can use only in web-browser-based application development. It exports react-router as a dependency and has additional DOM (document object model) bindings such as <BrowserRouter> and <Link>.

### When to Use Which
####  react-router-dom when working on a web app, because it contains all the necessary common components and features essential for routing in a web application.

### How to Use React Router DOM
#### Step 1: Install Package
```
npm install react-router-dom
```
#### Step 2: Import <BrowserRouter>
```
import { BrowserRouter, Route } from 'react-router-dom';

function App() {
 return (
  <BrowserRouter>

  </BrowserRouter>
 );
}

export default App;
```
#### Step 3: Import and use the child component, <Route>.
```
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import About from './components/about';
import Home from './components/home';

function App() {
 return (
  <BrowserRouter>
   <div><Routes>
      <Route path="/" element={<Home />} />
      <Route path="/about" element={<About />} />
    </Routes>
   </div>
  </BrowserRouter>
 );
}
```

#### As the URL changes to the specified paths, the UI also changes to display the specific component. The following are several components that we can use in our application: 
#### <BrowserRouter>: BrowserRouter is a parent component in react-router-dom that stores all the other route components. Allowing the declaration of individual routes is the main functionality of using BrowserRouter in the application.
#### <Routes>: Routes is a new component introduced in v6 that replaces the switch component. 
#### <Route>: Route is the child component that renders a specific UI component when the URL matches the specified path. The path attribute specifies the path name we assign to the component and the element attribute refers to the component to render when the URL matches.
#### <Link>: As its name suggests, Link allows a user to navigate to another page by clicking on it. For instance, you can use it when creating the application’s navigation bar. 

```
function Navbar() {
  return (
    <nav>
          <Link to="/">Home</Link>
          <Link to="/profile">Profile</Link>
    </nav>
  )
}
```
### Handling 'Not Found' Pages
#### There may be instances when users attempt to access a path that does not exist within the application. In such instances, you can set an asterisk (*) as the path to direct the user to the Page Not Found page.
```
<BrowserRouter><Routes><Route path="/" element={<Home />} />
       <Route path="/about" element={<About />} />
       <Route path="*" element={<PageNotFound />} />
   </Routes>
</BrowserRouter>
```
#### In summary React Router is used in React applications to:
#### - Enable navigation between different views or pages within the application.
#### - Define URL patterns and route mappings for different UI components.
#### - Implement client-side routing, allowing for a more fluid and interactive user experience without full page reloads.
#### - Organize and structure the application's UI layout and navigation hierarchy.
#### - Support features such as nested routing, route parameters, and history management.

14. Cart
15. React Router and useCallback
16. Cocktails


NB: To resolve ERR_OSSL_EVP_UNSUPPORTED error, which is triggered by changes in OpenSSL 3.0 used by Node.js I used the following command in my terminal:
```
$env:NODE_OPTIONS="--openssl-legacy-provider" 
npm start
```
