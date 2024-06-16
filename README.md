# LoaderQuark for React

This quark is a simple loader plugin with adaptation for React.

## Installation

```sh
npm install loader-quark-react --save
```

## Setup
AnyComponent.jsx
```js
import {Loader} from "loader-quark-react"
```

## Basic Usage
AnyComponent.jsx
```jsx
import React from "react"
import {Loader} from "loader-quark-react"

const AnyComponent = () => {
  const [loading, setLoading] = React.useState(false)
  //...
  
  // Perform some data loading, for example some api call
  useEffect(() => {
    setLoading(true) // Set loading to true in the beginning
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => {
        // Do something with the data
      })
      .catch(error => console.error(error))
      .finally(() => setLoading(false)) // After the data is loaded, set loading to false
  }, [])
  
  return (
    <>
      <Loader loading={loading} type="spinner" primaryColor="#7842f5">
        <div>
          {/* ...Content to show after loading is done... */}
        </div>  
      </Loader>
    </>
  ) 
}

export default AnyComponent
```


# DOCS
Full docs at [https://www.quarksjs.com/library/loader-quark-react/getting-started](https://www.quarksjs.com/library/loader-quark-react/getting-started).

Source code at [https://github.com/SamuelSlavik/LoaderQuarkReact](https://github.com/SamuelSlavik/LoaderQuarkReact)

# SUPPORT
Please support us by starring the repository or donate at [https://www.quarksjs.com/donate](https://www.quarksjs.com/donate) to help us maintain the project and cover hosting expenses.