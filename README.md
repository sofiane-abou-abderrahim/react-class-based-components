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

## 3. The Component Lifecycle (Class-based Components Only!)

1. add the `UserFinder.js` component
2. get rid of the `DUMMY_USERS` & refer to `this.props.users` instead of it in `Users.js`
3. output the `<UserFinder>` component instead of the `<Users>` component in `App.js`
4. add the `UserFinder.module.css` file

## 4. Lifecycle Methods In Action

1. convert the `UserFinder.js` component into a class-based component
2. use the `componentDidUpdate()` lifecycle to handle side effects and replace `useEffect()`
3. use `componentDidMount()` to simulate a case where the data comes from an http request
4. use `componentWillUnmount()` in `User.js`

## 5. Class-based Components & Context

1. add a new `users-context.js`
2. use context with the first approach: the context `Consumer` component by adding `<UsersContext.Consumer>` in `UserFinder.js`
3. or use `static contextType` in `UserFinder.js`
4. now access the context with `this.context.users` instead of `DUMMY_USERS`

## 6. Introducing Error Boundaries

1. simulate a server error by throwing an error in the `componentDidUpdate` lifecycle method in `Users.js`
2. use `try` / `catch` to prevent the app from crashing
3. if you throw an error in a component and want to handle it in a parent component, build an error boundary
4. add a `ErrorBoundary.js` file
5. build a class-based component named `ErrorBoundary`
6. use the `componentDidCatch()` lifecycle method which is going to be triggered whenever a child component throws an error
7. in `UserFinder.js`, wrap the `<ErrorBoundary>` component around the `<Users>` component
8. cacth the error with `componentDidCatch()`
