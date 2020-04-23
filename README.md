### React 

```
├── hooks
├── assets
├── components
├── pages
├── services
│
├── contexts
├── actions
├── reducers
├── store
│
├── utils.js
└── routes.js
```

### useContext

```js
//contexts/UserContext

const UserContext = React.createContext(null);

//App

const App = props => {
    const context = useContext(UserContext);
    ...
};

<UserContext.Provider value = {...}>
    <App />
</UserContext.Provider>

```
