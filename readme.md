# Angular SPA Book page

Lesson from CodeCademy on Angular 1

[**Check online demo**](https://nobleworkshop.github.io/angular-01/)

Click on red circels - to add likes or dislikes to each book.

## Angular features

Angular module - to create the app
```JS
var app = angular.module("myApp", []);
```

Bind ang app to the page or part of the page

```html
<body ng-app="myApp">
```

Bind controller for Books
```html
<div class="main" ng-controller="MainController">
```

Scope properties to define Module properties
```JS
$scope.title = 'Top Sellers in Books';
```

Scope propertie with array of objects. Books collection:
```JS
$scope.products = 
[ 
	{ 
		name: 'The Book of Trees', 
		price: 19, 
		pubdate: new Date('2014', '03', '08'), 
		cover: 'img/the-book-of-trees.jpg',
		likes: 0,
		dislikes: 0
	}, 
	{ 
	    ...
	 } 
],
```

Scope properties as a functions
```JS
$scope.plusOne = function(index){
		$scope.products[index].likes += 1;
},
```

Show variables from scope in HTML
```html
{{ title }}
{{ product.name }}
```


## Directives

ng-repeat directive to loop throught array
```html
<div ng-repeat="product in products" class="col-md-6">
```

ng-src directive to bind images src attribute to scope variables
```html
<img ng-src="{{ product.cover }}">
```

ng-src directive to bind function on click for element
```html
<p class="likes" ng-click="plusOne($index)">
```
