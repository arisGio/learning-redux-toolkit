# Learning Redux Toolkit aka RTK

## Why you should take this course

- redux stores
- reducers
- actions
- slices
- making APi requests by building a shopping app

## What you're going to build

- js
- function components
- react hooks

## Why Redux Toolkit?

- Redux Toolkit

  - state management in react apps
  - toolset for efficient Redux development

- Redux

  - open source library for managing & centralizing your application state

- Redux Toolkit

  - Standard way to write Redux logic

- 3 common concerns

  - complications
  - packages
  - boilerplate code

- Redux Core Library

- redux toolkit

  - out of the box all of the functionality that Redux would have, only when combined with additional libraries

- Redux Toolkit
  - best practices
  - good default behaviours
  - catching mistakes
  - simpler code

## Chapter: 1. Understanding Redux

### Working with Redux actions and reducers

- 3 building parts for Redux to work

  - ACTIONS
  - REDUCERS
  - STORE

- ACTIONS
  - objects that we use to send data to the Redux store

<code>
{
   payload: data_for_the_store,
   type: do_something_in_the_store
}
</code>

<code>
{
   payload: [Object, Array, string, ...],
   type: "string"
}
</code>

- REDUCERS

  - use actions to know what to do with our Redux store
  - Reducer > Action > Store

- reducers are pure functions that have the current application states & intended actios as their first 2 parameters

<code>
const reducer = ( state, action ) => {
   const { type, payload } = action 
   // use the action to modify the state
} 
</code>

### How the Redux store works

- The STORE

  - only one store in an app
  - keep app state

- allows to access state
  - getState()
  - update()

<code>
store.update()</code>

- actions tell the reducers how to interact with the store

- store allows the reducers to access & modify the application state

<code>
import { configureStore } from '@reduxjs/toolkit'

const store = configureStore({
reducer: reducer_value
})
</code>

<code>store.getState()</code>

<code>>store.dispatch(action)</code>

### Working with slices in Redux Toolkit

- A redux app can have as many slices as it's needed to represent each part of the application

<code>
import { createSlice } from '@reduxjs/toolkit'

const mySlice = createSlice({
name: 'my slice',
initialState: [],
reducer: {
doSomething: (state, action) => {
// use the action to do something with the state
}
},
extraReducers: {}
})
</code>

## 2 - Setting up Your App

### Setting up your base project

- installed Bootstrap to focus on Redux and use ready made styles
- project structure
  - data
  - components
  - styles
- empty-cart show when there's no item in the cart
