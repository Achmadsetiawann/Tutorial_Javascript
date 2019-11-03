<h2><p align="center"> Tutorial Javascript Syntax </h2>
<hr/>
<div><h3>Structure React <h3/></div>
<br> Module <br>
npx create-react-app my-app // this for create react library <br>

<br>

```javascript
import React, { Component } from "react";
import logo from "./logo.svg";
import "./App.css";

class App extends Component {
  constructor() {
    super();
    this.state = {
      yourstate: "this.state.yourstate"
    };
  }

  render() {
    return <div className="App">{this.state.yourstate}</div>;
  }
}

export default App;
```

<hr/>
<div><h3>Next Tutor<h3/></div>

Event Button with Arrow Syntax

```javascript
<button onClick={() => this.setState({ yourstate })}>
  Event Onclick yourstate
</button>
```

Map Function

```javascript
class App extends Component {
  constructor() {
    super();
    this.state = {
      yourcode: [
        {
          name: "Achmad"
        },

        {
          name: "Setiawan"
        },

        {
          name: "Wawan"
        }
      ]
    };
  }

  render() {
    return (
      <div className="App">
        {this.state.yourcode.map(yourcode => (
          <h1> {yourcode.name} </h1>
        ))}
      </div>
    );
  }
}
```

<br> ComponentDidMount <br>
Structure componentDidMount() // Use to after state u can place that.
<br>

```javascript
componentDidMount() {

    fetch('https://jsonplaceholder.typicode.com/users')
    .then(response => response.json())
    .then(users => console.table(users));

  }
```

<hr/>
<div>
    <p>
    Lets Try and enjoy your life quotes. <br>
    #Dreamer, work hard and spend of time to learn code. make my dream come true.
    </p>
</div>

<!-- <div align ="center">
<img src="https://github.com/Achmadsetiawann/Android_MyRecyclerView/blob/master/proof.gif" width="200" height="300">
</div> -->
