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

<UserContext.Provider value = {...}>
    <App />
</UserContext.Provider>

```
