##### What is the role of Redux Thunk middleware?

<details>
  <summary>Answer</summary>
  It allows you to write action creators that return a function instead of an action.<br>
  Can handle async code this way
</details>



##### Describe why it is useful to use redux; in what cases does it make sense to not use it?

<details>
  <summary>Answer</summary>
  As an application grows, managing its state can become difficult. Passing functions and params to grandchildren 
  or great grandchildren components becomes cumbersome.<br>
  It is not necessary to use in small applications where state can be managed in an easier fashion
</details>


##### At a highlevel, what are some of the necessary steps setup redux in an application?

<details>
  <summary>Answer</summary>
  wrap app component with Provider<br>
  create a store file to mng state <br>
  create/combine reducers <br>
  mapStateToProps, mapDispatchToProps using connect
</details>


##### Describe the lifecycle of a component state change when using redux.

<details>
  <summary>Answer</summary>
  User input prompts an Action, which sends a request to the database.  The Action dispatches the
  response (type and payload) to the appropriate Reducer action, which then updates the state
  and re-renders the component(s).
</details>

##### How do you pull parameters from a url when rendering a new component? Why is storing information in the URL useful?

Describe the lifecycle of a component state change.

<details>
  <summary>Answer</summary>
  when you pass a function into the render attribute of Route, it can take one arg - match <br>
  Can bookmark sites and rendera a page properly based on URL params
</details>

##### What does the following code need to pass?

```javascript
  const ProfilesList = ({ profiles }) => {
    const cards = profiles.map(profile => {
      return (
        <div key={ profile.username } className="card m-2 border" style={{ minWidth: '14rem', maxWidth: '14rem' }}>
          <img className="card-img-top" src={ profile.avatar } alt={ profile.username } />
          <div className="card-body">
            <h5 className="card-title">{ profile.username }</h5>
            <Link to=`/profiles/${profile.username}` className="btn btn-primary">View</Link>
          </div>
        </div>
      )
    })

    return <section className="card-group">{ cards }</section>
  }
```

<details>
  <summary>Answer</summary>
  The <Link> "to" value needs to be wrapped in { } to be read by JSX
</details>

##### Is it possible to conditionally render the Candidate component?  If so, how?

```javascript
<div>
  <Candidate castVote={ this.castVote } />
</div>
```

<details>
  <summary>Answer:</summary>
  "If" is a protected keyword, so you can't just open some { } and throw a conditional inside. Use ternary operators instead.
  
  i.e.
  ```javascript
  <div>
    {
      this.state.isLoading ? <Spinner message="Loading..." /> : <Candidate castVote={ this.castVote } />
    }
  </div>
  ```
</details>
