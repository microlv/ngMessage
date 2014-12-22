# ngMessage v1.0.1
=========

message for angular, different with $scope.$emit/$broadcast, this use single service(like message center) to register and send.
currently not support promise and mulit message.
more demo can see app.js and index.html

## Download

Check out [https://github.com/lvjianyu/ngMessage.git] for details over the differences between builds.

Wiki: http://lvjianyu.github.io/ngMessage   (not finished)

## Features

message center base on angularjs.
you can use the message to inform other controller(which still not init) or service or
factory(which use to handle something like something changed and the factory need to automation change property too)



## Support

Currently only test in Chrome, require angularjs

## Installation & usage

In browsers:

```html
<script src="ngMessage.js"></script>
```

Using [`bower`](http://bower.io/):

```js
bower install ng-message -S
```

```js
	inject ngMessage
    var app = angular.module('app', ['ngMessage']);
```

```
    //register message, alias use: on, bind,etc.
    ngMessage.register('1.register', function (k) {
            console.log('1.response1');
        });
```

```
    //fire the message
    ngMessage.trigger('1.register', [{a: 1}, {a: 2}]);
```


## Author

Andy.lv@live.com;
Any problem contact with me.

## Contributors
