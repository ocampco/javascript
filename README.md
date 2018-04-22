# :star: JavaScript Style Guide

## Table of Contents
  1. [Components](#components)

## Components

```js
// Stateless

import React from 'react';
import PropTypes from 'prop-types';

const StatelessComponent = ({ a }) => (
  <div>`${a}`</div>
);

StatelessComponent.propTypes = {
  a: PropTypes.string.isRequired,
};

export default StatelessComponent;

```

```js
// Class

import React, { Component } from 'react';
import PropTypes from 'prop-types';

import SomeComponent from ./SomeComponent;

class SomeClass extends Component {
  state = {
    hidden: true,
  }

  handleClick = (event) => {
    event.preventDefault();
  }

  toggleHidden = () => {
    this.setState({ hidden: !this.state.hidden });
  }

  render() {
    const { a } = this.props;
    const { hidden } = this.state;
    
    return (
      <div>
        { hidden && <SomeComponent a={a}> }
        <button onClick={this.handleClick}/>
      </div>
    );
  }
}

SomeClass.propTypes = {
  a: PropTypes.string.isRequired,
};

export default StatelessComponent;
```

  
