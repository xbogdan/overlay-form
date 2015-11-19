# Overlay Form
Creates an overlay containing a form with your wanted fields.

# Usage
```javascript
var overlayForm = new of({
  fields: [
    {
      label: 'Name',
      inputType: 'text',
      inputName: 'name-field'
    },
    {
      label: 'Password',
      inputType: 'password',
      inputName: 'password-field'
    }
  ],
  finishCallback: function(data) {
    console.log(data);
  }
});
```

<br>
# Fields
`inputName` field is optional. If it is not set the name of the input is
```javascript
label.split(' ').join('-').toLowerCase();
```
<hr>
`data` argument of the `finishCallback` function is an `array` of js objects where <br>
`name` is the `inputName` field
```javascript
{
  name: 'name-field',
  value: 'John'
}
```
