# Creating the Routes

The following pages in the app are as follows.

##### Users

/login

/users

/users/create

/users/edit

##### Questions

/questions

/questions/:questionId



## Install React Router

```bash
npm install --save react-router-dom
```

### Browser Router

Listen for changes in the URL and make sure the correct screen appears when the URL changes.

#### **Import Browser Router**

```bash
import { BrowserRoter } from 'react-router-dom' 
```

#### **Wrap our main app in BrowserRouter**

```react
import React from "react";
import ReactDOM from "react-dom";
import App from "./App.js";

import { BrowserRouter } from 'react-router-dom';

ReactDOM.render(
<BrowserRouter>
    <App />
</BrowserRouter>, document.getElementById("root"));
```

#### The Link Component

Import the **Link** component on the pages that need links. 

```bash
import { Link } from 'react-router-dom' 
```

To create a link

```react
<Link
	to='/login'
	className='btn-login'
>
    Login
</Link>
```

### Routes

```react
<Route path='/' exact component={HomePage} />

```

