*This repository is a mirror of the [component](http://component.io) module [ianstormtaylor/bind](http://github.com/ianstormtaylor/bind). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/ianstormtaylor-bind`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# bind
  
  A clear API for function binding helpers.

## Installation

    $ component install ianstormtaylor/bind
    $ npm install ianstormtaylor/bind

## Example

```js
var bind = require('bind');

var object = {
  one: function(){},
  two: function(){}
};

// bind a single method
object.one = bind(object, object.one);

// bind certain methods
bind.methods(object, 'one', 'two');

// bind all methods
bind.all(object);
```

## API

### bind(object, function)

  Bind a `function` to always be called with the `object` as context.

### bind.all(object)
  
  Bind all methods on an `object` to always be called with the `object` as context.

### bind.methods(object, methods...)

  Bind certain `methods` on `object` to always be called with the `object` as context.

## License

  MIT
