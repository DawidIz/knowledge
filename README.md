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


```js
const Flex = styled.div`
    display: flex;
    flex-flow: ${props => props.flexFlow};
    justify-content: ${props => props.justifyContent};
    align-items: ${props => props.alignItems};
    align-content: ${props => props.alignContent};
`

const Card = styled.div`
    flex: 1;
    background-color: #5e7491;
    border-radius: 0.4rem;
`

const Text = styled.p`
    margin: 0;
    padding: 1rem;
`

const CardHeader = ({ title, subtitle }) => {
    return (
        <div>
            <Flex flexFlow='column' alignItems='center'>
                {title && <span>{title}</span>}
                {subtitle && <span>{subtitle} </span>}
            </Flex>
        </div>
    )
}

const CardMedia = ({ image }) => {
    return (
        <div
            style={{
                backgroundImage: `url(${image})`,
                backgroundSize: 'cover',
                backgroundPosition: 'center',
                height: 0,
                paddingTop: 50 + '%',
            }}
        ></div>
    )
}

const CardContent = ({ text }) => {
    return <Text>{text}</Text>
}

const CardActions = () => {
    return (
        <Flex justifyContent='space-around'>
            <button>&lt;3</button>
            <button>Share</button>
            <button>expand</button>
        </Flex>
    )
}

const CardCollapse = ({ text }) => {
    return <Text>{text}</Text>
}

export default () => {
    return (
        <Card>
            <CardHeader
                title={'Chilli con carne'}
                subtitle={new Date().toDateString()}
            />
            <CardMedia image={chilli} />
            <CardContent text={'example text'} />
            <CardActions />
            <CardCollapse text={'collapse text'} />
        </Card>
    )
}


```
