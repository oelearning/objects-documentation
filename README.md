# Chapter 4: Objects basics

This repo is to document the basics about objects in JavaScript. All information used as a reference the book [JavaScrip Info](http://javascript.info)

## Objects

In JavaScript there are **8 data types** seven of them are called _"primitive"_, because their values contain only a single thing (be it a string or a number).

In constrast, objects are used to store keyed collections of various data and more complex entities.

An object can be created with figure brackets `{}` with an optional list of properties. **A property is a "key:value" pair**, where `key` is a string (also called a "property name"), and `value` can be anything.

We can imagine an object as a cabinet with files. Every piece of data is stored in its file by the key, it's easy to find a file by its name or add/remove a file.

![object analogue of a cabinet with files](./assets/img/figure1.png)

An empty object ("empty cabinet") can be created using of two syntaxes:

```
let user = new Object(); // "object constructor" syntax
let user = {}; // "object literal" syntax
```

![empty object representation](./assets/img/figure2.png)

It's more common to use figure brackets to declare an empty object. That declaration is called an _object literal_.

## Literals and properties

We can create some properties into `{}` as "key: value" pairs.

```
let user = {     // an object
  name: "John",  // key "name" store value "John"
  age: 30        // key "age" store value 30
};
```

A property has a key (also known as "name" or "identifier") before the colon `":"` and a value to the right of it.

In the `user` object, there are two properties:

1. The first property has the name `"name"` and the value `"John"`.
2. The second one has the name `"age"` and the value `30`.

The resulting `user` object can be imagined as a cabinet with two files labeled "name" and "age".

![representation of user object declared above](./assets/img/figure3.png)

We can add, remove and read files from it at anytime. Property values are accessible using the dot notation.

```
// get property values of the object:

alert( user.name ); // John
alert( user.age ); // 30
```

The value can be of any typ, Let's add a boolean one:

```
user.isAdmin = true;
```

![adding the property isAdmin: true to the user object](./assets/img/figure4.png)

To remove a property, we can use the delete operator:

```
delete user.age;
```

![property age deleted](./assets/img/figure5.png)

We can aslo use multiword property names, but then they must be quoted.

```
let user = {
  name: "John",
  age: 30,
  "likes birds": true  // multiword property name must be quoted
};
```

![creating a multiword property](./assets/img/figure6.png)

> Note: The last property in the list may end with a comma:

```
let user = {
  name: "John",
  age: 30,
}
```

This is called a "trailing" o "hanging" comma. Makes it easier to add/remove/move around properties, because all lines become alike.
