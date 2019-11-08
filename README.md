# Why did you update

> Compatible with any Redux version!

[![npm version](https://badge.fury.io/js/why-did-you-update-redux.svg)](https://badge.fury.io/js/why-did-you-update-redux)

Why did you update is a function that monkeypatches Redux and notifies you in the console when **potentially** unnecessary re-renders occur
driven by unnecessary updates from `mapStateToProps`, which means - your selectors, or memoization is not as good, as they should.

Fear not, `why-did-you-update-redux` will tell you which field is updated while it should not, so you can fix it.

![](https://i.imgur.com/73vmgG1r.png)

Look at the report - something is wrong with __minDate__, and __maxDate__. With "proper" memoization applied - they should be equal to the previous values, that's the idea of memoization, but something went wrong.
Could you please double check your code? (Just click on the function to jump straight into definition)

### Setup
This library is available on npm, install it with: 
`npm install --save why-did-you-update-redux` 
or 
`yarn add why-did-you-update-redux`.

### Usage
```js
import 'why-did-you-update-redux'; 
// import before redux!
```
What's all, and it will remove itself from a production bundle, so you don't have to.

### How it works

This is basically `import 'beautiful-react-redux/check'`, see 
[beautiful-react-redux](https://github.com/theKashey/beautiful-react-redux) for more information.

`why-did-you-update-redux` is based on memoize-state library - [How I wrote the world’s fastest React memoization library](https://itnext.io/how-i-wrote-the-worlds-fastest-react-memoization-library-535f89fc4a17)

### Example?
[https://codesandbox.io/s/o4mrzr865](https://codesandbox.io/s/o4mrzr865)

### License

MIT
