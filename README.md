# Class-Based Components

## An Alternative Way Of Building Components

- What & Why?
- Working With Class-based Components
- Error Boundaries

# Steps

## 0. Starting Project

1. run `npm install`
2. run `npm start`
3. create `README.md`

## 1. Adding a First Class-based Component

1. define a new class named `User` in `User.js`
2. import `component` from React & extend it on the `User` class
3. access the `props` property with help of the `this` keyword

## 2. Working with State & Events

1. convert the `Users.js` functional component into a class-based component
   1. create a class named `Users`
   2. add a method named `toggleUsersHandler` in this class
   3. define state with help of the `constructor` method to initialize it
   4. change your state by calling the special `setState` method
2. render this state in the `render` method
3. derive the `userList` inside the `render` method as well
4. make the `this` keyword in the `toggleUsersHandler` function refers to the surrounding class by binding `this`
5. call the `toggleUsersHandler` function in the `render` method
6. call super constructor in derived class because when you add the `constructor` to your class and you extend another class, you need to call super which calls the constructor of the `super()` class so if the class were inheriting from (`Component`)
