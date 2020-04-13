# The Constructor Pattern

## Object Creation

```js
// Each of the following options will create a new empty object:
  
var newObject = {};
  
// or
var newObject = Object.create( Object.prototype );
  
// or
var newObject = new Object();
```

```js
function Car( model, year, miles ) {
 
  this.model = model;
  this.year = year;
  this.miles = miles;
 
}
 
 
// Note here that we are using Object.prototype.newMethod rather than
// Object.prototype so as to avoid redefining the prototype object
Car.prototype.toString = function () {
  return this.model + " has done " + this.miles + " miles";
};
 
// Usage:
 
var civic = new Car( "Honda Civic", 2009, 20000 );
var mondeo = new Car( "Ford Mondeo", 2010, 5000 );
 
console.log( civic.toString() );
console.log( mondeo.toString() );
```

Above, a single instance of toString() will now be shared between all of the Car objects.