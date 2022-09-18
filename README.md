# change-json-case
How to change JSON properties to uppercase, lowercase or capitalised


** CHANGE TO UPPERCASE **
```
JSON.parse('{"Test": {"Foo": 1, "Bar": 2} }', function(prop, value) {
  var lower = prop.toUpperCase();
  if(prop === lower) {
  console.log(value);
  	return value;
  }else {
  	this[lower] = value;
  }
});
```

** CHANGE TO LOWERCASE **

```
JSON.parse('{"Test": {"Foo": 1, "Bar": 2} }', function(prop, value) {
  var lower = prop.toLowerCase();
  if(prop === lower) {
  console.log(value);
  	return value;
  }else {
  	this[lower] = value;
  }
});
```


** CHANGE TO CAPITALISED **

```
JSON.parse('{"Test": {"Foo": 1, "Bar": 2} }', function(prop, value) {
  var lower = prop.charAt(0).toUpperCase() + prop.substring(1);
  if(prop === lower) {
  console.log(value);
  	return value;
  }else {
  	this[lower] = value;
  }
});

```