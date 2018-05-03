# React Freshchat
React Freshchat is a wrapper on top of Freshchat (see oficial doc here https://developers.freshchat.com/).

## How to use
**DO NOT INCLUDE Freshchat script in `head`, React Freshchat will automatically add it with lazy load technique**

* Install `electron-react-freshchat` (see Installation).
* Import the lib where you initialize your React App.
* Include the component with the `token`.

### Example

```
import React from 'react'
import FreshChat from 'electron-react-freshchat'

class App extends React.Component {
  // ...
  render() {
    return <div>
      <FreshChat
        token={config.freshchat.token}
        email: 'user@email.com',
        first_name: '...',
        onInit={widget => {
          /* Use `widget` instead of `window.fcWidget`
            widget.user.setProperties({
              email: user.email,
              first_name: user.firstName,
              last_name: user.lastName,
              phone: user.phoneNumber,
            })
          */
        }}
      />
    </div>
  }
}
```

For more details: https://developers.freshchat.com/

## Installation
Only NPM is supported for now: `npm i -s electron-react-freshchat`

## UMD Support
UMD is supported out of the box.

## TODO
* Unit Testing
* Integrate Webpack
