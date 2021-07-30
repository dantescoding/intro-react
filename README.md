This is your template repository!

You will make all changes in the `changes` branch.

This repository is licensed under [MIT](../LICENSE) (c) 2019 GitHub, Inc.


**Props are the input to components.***


#### Example of passing functions as props
So where exactly are those functions we created to set state getting called?

On line 63 in src/App.jsx, it looks like we pass the addAssignment function as a prop in this chunk of code.

Navigate to src/List.jsx and take a look at the code between lines 18 and 25 in src/List.jsx.
~~~
handleSubmit(event) {
    this.setState({
      value: ""
    });

    this.props.addFunction(this.state.value);
    event.preventDefault();
}
~~~
**When the submit button is clicked, we call the addFunction with the value of our input box. For assignments, the addFunction references the this.addAssignment in App. So when we call this.props.addFunction, we are calling back to the parent component and using the parent's function.**
