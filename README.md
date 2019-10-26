<h2><p align="center"> Tutorial Javascript Syntax </h2>
<hr/>
<div><h3>Structure React <h3/></div>

``` javascript
import React, { Component } from 'react';
import logo from './logo.svg';
import './App.css';

class App extends Component { 
  
  constructor() {
    super();
    this.state = {
      yourstate : 'this.state.yourstate'
    };

  }
  
  render(){ 
    return(
    <div className="App"> 
    {this.state.yourstate}
    </div>
    ); 
  } 
} 

export default App;
```
<hr/>
<div><h3>Next Tutor<h3/></div>
<div>Event Button with Arrow Syntax</div>
``` javascript
<button onClick={() => this.setState ({ yourstate }) }>
          Event Onclick yourstate
</button>
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