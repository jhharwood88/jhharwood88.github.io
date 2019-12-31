---
layout: post
title:      "Props VS state in React "
date:       2019-12-31 22:08:35 +0000
permalink:  props_vs_state_in_react
---


In  React, props are variables passed to it by its parent.  However, State is comprised of variables passed down by the component by which it is created and managed by. State is something that can be created by the use of props. As an example, a parent component could include a child by calling 

```
<Child />

```
This would then allow the parent component to pass it props, such as

```
<Child name=bill/>

```
Within the child constructor, we could then access this exact same prop in this manner:

```
class Child extends React.Component {
  constructor(props) {
    super(props)
    console.log(props.name)
  }
}

```
This will also allow access for any other method in this class to call on this set of props to access the information held within name, using this.props

You can also use props to help set state within the constructor function by directly setting state based on props as such:

```
class Child extends React.Component {
  constructor(props) {
    super(props)
    this.state.name = props.name
  }
}

```
While components can derive state from props, its important to note that a component can initialize its state without referencing props. It is a general convention that props should not be modified within a component, if changes are to be made within the child it should be reflected on the change in that components state. One of the main benefits of child components inheriting form its parent components props is that they are allowed access to method in the parent component. While state is an important part of understanding the benefits of the React framework, most of your components will display information from inherited props and will never have a state.

