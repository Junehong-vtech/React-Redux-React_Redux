# React-Redux-React_Redux
### React
The library for web and native user interfaces.
### Redux
A JS library for predixtable and maintainable global state management.
### React Redux
The offical React UI binding layer for Redux. It lets your React components read data from a redux store, and dispatch actions to the store to update state. 
#### Create React App
`$ mkdir react-app`  
`$ cd react-app`  
`react-app$ npx create-react-app .`  
#### Edit React App
- `public/index.html` -> `src/index.js` -> `src/App.js`  
- `src/index.css` and `src/App.css`
## APIs
#### createRoot()
Create a root to display React components inside a browser DOM node.
- render() : Disaply a piece of JSX ("React node") into the React root's browser DOM node.
#### createStore()
Creates a Redux store that holds the complete state tree of your app. There should only be a single store in your app.
#### Store
A store holds the whole state tree of your application. The only way to change the state inside it is to dispatch an action on it, which triggers the root reducer function to calculate the new state.  
- getState() : Returns the current state tree of your application. It is equal to the last value returned by the store's reducer.  
- dispatch(action) : Dispatches an action. This is the only way to trigger a state change.
#### Provider
The `<Provider>` component makes the Redux `store` available to any nested components that need to access the Redux store.

#### connect()
The `connect()` function connects a React component to a Redux store.
#### bindActionCreators()
The only use case for bindActionCreators is when you want to pass some action creators down to a component that isn't aware of Redux, and you don't want to pass dispatch or the Redux store to it.
#### reduxForm()
Creates a decorator with which you use redux-form to connect your form component to Redux. It takes a config parameter which lets you configure your form.

#### Hooks
React's "hooks" APIs give function components the ability to use local component state, execute side effects, and more.  
Hooks allow function components to have access to state and other React features. Because of this, class components are generally no longer needed.
##### useSelector()
Allow you to extract data from the Redux store state for use in this component, using a selector function.
##### useDispatch()
This hook returns a reference to the dispatch function from the Redux store. You may use it to dispatch actions as needed.
##### useEffect
The useEffect Hook allows you to perform side effects in your components.  
`useEffect` is a React Hook that lets you synchronize a component with an external system.  
Some examples of side effects are: fetching data, directly updating the DOM, and timers.  
`useEffect(setup, dependencies?)`  
###### Parameters
- `setup`: The function with your Effect’s logic. Your setup function may also optionally return a cleanup function. When your component is added to the DOM, React will run your setup function. After every re-render with changed dependencies, React will first run the cleanup function (if you provided it) with the old values, and then run your setup function with the new values. After your component is removed from the DOM, React will run your cleanup function.  
- optional `dependencies`: The list of all reactive values referenced inside of the setup code. Reactive values include props, state, and all the variables and functions declared directly inside your component body. If your linter is configured for React, it will verify that every reactive value is correctly specified as a dependency. The list of dependencies must have a constant number of items and be written inline like [dep1, dep2, dep3]. React will compare each dependency with its previous value using the Object.is comparison. If you omit this argument, your Effect will re-run after every re-render of the component.  
##### useState
The useState Hook allows us to track state in a function component.  
useState accepts an initial state and returns two values:  
  `The current state.`  
  `A function that updates the state.`  
  `// const _mode = useState('WELCOME');`  
  `// const mode = _mode[0];`  
  `// const setMode = _mode[1];`  
  `const [mode. setMode] = useState('WELCOME');`  
##### useMemo
The React `useMemo` Hook returns a memoized value. `Think of memoization as caching a value so that it does not need to be recalculated.`  
The `useMemo` Hook only runs when one of its dependencies update.  
This can improve performance.  

