# React

## *- State*

### all state must be immutable.  

##### *Exemple:*

```javascript
  state = {
    newValue: '',
    values: ["NodeJS", "React", "React Native"]
  };

  handleAlteration = e => {
    e.preventDefault();
    this.setState({ values: [...this.state.values, this.state.newValue] });
  }

  //PS: (...) its an spread operator:
  // https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Spread_operator
```

## *- Properties*

### we send the property to function this way.  

##### *Exemple:*

```javascript
  <ul>
  {this.state.techs.map(tech => (
    <TechItem
      key={tech}
      tech={tech} //property value
      onDelete={() => this.handleDelete(tech)} // property Function
    />
  ))}
```

### we can call the properties of two forms:

##### *in Class*

```javascript
  class MyComponent extends Component{
    render() {
      this.props.{nameProp};
    }
  }
```

##### *in Function*

```javascript
  Function MyComponent({nameProp}){
    this.nameProp;
  }
```

### we can set to an property with default:

##### *React Standard*

```javascript
  Function MyComponent({nameProp}){
    this.nameProp;
  }

  MyComponent.defaultProps = {
    nameProp: 'value'
  }
```

##### *with deconstruction*

```javascript
  Function MyComponent({nameProp = 'value'}){
    this.nameProp;
  }
```
