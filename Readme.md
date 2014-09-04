#React Validating Form

##Example

```javascript
var Example1 = React.createClass({

  handleSubmit: function(){
    alert(JSON.stringify(this.refs.form.getValue()));
  },

  render: function(){
    var wrapperClassName='col-xs-12';
    return (
      <Well className="example">
        <ValidatingForm
          schema={userSchema}
          onSubmit={this.handleSubmit}
          submitLabel="Register"
          ref='form'
          horizontal>
          <ValidatingInput
            field='username'
            placeholder='Enter Username'
            wrapperClassName={wrapperClassName}/>
          <ValidatingInput
            field='password'
            type='password'
            placeholder='Enter Password'
            wrapperClassName={wrapperClassName}/>
          <ValidatingInput
            field='passwordCheck'
            type='password'
            placeholder='Re-enter Password'
            wrapperClassName={wrapperClassName}/>
        </ValidatingForm>
      </Well>
    );
  }
});
```