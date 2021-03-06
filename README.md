# React ES6 ProgressBar.js

### A React component library that implements [kimmobrunfeldt's ProgressBar.js](https://github.com/kimmobrunfeldt/progressbar.js) with full options support.

## Installation

```
$ npm install --save react-es6-progressbar.js
```

## Usage
```
import React, { Component } from 'react';
import { Circle, SemiCircle, Line } from 'react-es6-progressbar.js'

class App extends Component{

  const circle_options = {
    text: 'test',
    style: {
      color: 'green'
    }
  };

  const semicircle_options = {
    text: {
      value: 'semicircle test',
      color: 'rgba(255, 255, 255, 0.6)
    },
    color: '#333',
    duration: 1000
  };

  const line_options = {
    color: 'red',
    easing: 'easeOut',
    strokeWidth: '5'
  };

  render(){

    return(

      <Circle progress={0.75} options={circle_options} container_style={{height: '200px', width: '200px'}} />
      <SemiCircle progress={0.33} options={semicircle_options} container_style={{height: '200px', width: '200px'}} />
      <Line progress={1.0} options={line_options} container_style={{height: '200px', width: '200px'}} />

    );

  }

}
```

## Props

| Prop | Type | Default | Usage |
|------|:------:|:-------:|-------|
| container_class | **String** | *null* | Class to be added to container element                                                                                                   |
| container_style | **Object** | *null* | CSS styles for the container element                                                                                                     |
| progress        | **Number** | *0.5*  | [ProgressBar.js progress amount](http://progressbarjs.readthedocs.io/en/latest/api/shape/#animateprogress-options-cb) from 0 to 1, where 1 is 100% of the distance.     |
| options         | **Object** | *null* | [ProgressBar.js shape container options](http://progressbarjs.readthedocs.io/en/latest/api/shape/#new-shapecontainer-options)            |

## Licence
MIT