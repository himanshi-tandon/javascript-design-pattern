# Javascript Design Pattern

<ul>
  <li><a href="#creational" title="Creational">Creational</a>
    <ul>
      <li><a href="#factory-pattern" title="Factory Pattern">Factory Pattern</a></li>
      <li><a href="#constructor-pattern" title="Constructor Pattern">Constructor Pattern</a></li>
      <li><a href="#singleton-pattern" title="Singleton Pattern">Singleton Pattern</a></li>
      <li><a href="#prototype-pattern" title="Prototype Pattern">Prototype Pattern</a></li>
    </ul>
  </li>
  <li><a href="#structural" title="Structural">Structural</a>
    <ul>
      <li><a href="#module-pattern" title="Module Pattern">Module Pattern</a></li>
      <li><a href="#adapter-pattern" title="Adapter Pattern">Adapter Pattern</a></li>
      <li><a href="#decorator-pattern" title="Decorator Pattern">Decorator Pattern</a></li>
      <li><a href="#façade-pattern" title="Façade Pattern">Façade Pattern</a></li>
      <li><a href="#mixin-pattern" title="Mixin Pattern">Mixin Pattern</a></li>
      <li><a href="#flyweight-pattern" title="Flyweight Pattern">Flyweight Pattern</a></li>
    </ul>
  </li>
  <li><a href="#behavioral" title="Behavioral">Behavioral</a>
    <ul>
      <li><a href="#mediator-pattern" title="Mediator Pattern">Mediator Pattern</a></li>
      <li><a href="#observer-pattern" title="Observer Pattern">Observer Pattern</a></li>
    </ul>
  </li>
</ul>

## Creational

#### Factory Pattern
#### Constructor Pattern

```javascript
// traditional Function-based syntax
function Hero(name, specialAbility) {
  // setting property values
  this.name = name;
  this.specialAbility = specialAbility;

  // declaring a method on the object
  this.getDetails = function() {
    return this.name + ' can ' + this.specialAbility;
  };
}

// ES6 Class syntax
class Hero {
  constructor(name, specialAbility) {
    // setting property values
    this._name = name;
    this._specialAbility = specialAbility;

    // declaring a method on the object
    this.getDetails = function() {
      return `${this._name} can ${this._specialAbility}`;
    };
  }
}

// creating new instances of Hero
const IronMan = new Hero('Iron Man', 'fly');

console.log(IronMan.getDetails()); // Iron Man can fly
```

### Singleton Pattern
#### Prototype Pattern

## Structural
#### Module Pattern

```javascript
var Module = (function() {
    function privateMethod() {
        // do something
    }

    return {
        publicMethod: function() {
            // can call privateMethod();
        }
    };
})();

Module.publicMethod(); // works
Module.privateMethod(); // Uncaught ReferenceError: privateMethod is not defined

/*------------------OR-----------------------*/
var Module = (function () {
    function _privateMethod() {
        // do something
    }
    function publicMethod() {
        // do something
    }
    return {
        publicMethod: publicMethod,
    }
})();
```

#### Adapter Pattern
#### Decorator Pattern
#### Façade Pattern
#### Mixin Pattern
#### Flyweight Pattern

## Behavioral
#### Mediator Pattern
#### Observer Pattern

#### References
- https://medium.com/better-programming/javascript-design-patterns-25f0faaaa15
