# `Template: Json Schema Validation`
![Java CI](https://github.com/anilkulkarni87/JsonSchema/workflows/Java%20CI/badge.svg?branch=master)

This is a template project for implementing json schema validations. Json schema can be defined
for any complex structure. I think that is the most time consuming part, but once defined correctly
it provides a very effective validate json data files. 
* [**Json Schema file**](src/main/resources/customer_schema.json)
* [**Json data files**](src/main/json/)

### Steps:
* Define schema for the json objects
* Create sample json files

### How to execute:
```
gradle clean validateCustomJson
```

#### Output for current schema and json files
```text
* What went wrong:
Execution failed for task ':validateCustomJson'.
> One or more validation errors found against schema '\src\main\resources\customer_schema.json':
  File '\src\main\json\customer1.json' has 2 violations:
  #/customerIdentity/mid_name: expected maxLength: 6, actual: 7
  #/customerIdentity/first_name: expected maxLength: 4, actual: 6
  File '\src\main\json\customer2.json' has 2 violations:
  #/customerIdentity/mid_name: expected maxLength: 6, actual: 7
  #/customerIdentity/age: 22.0 is not a multiple of 3
```

### References
* [**Json Schema Official site**](http://json-schema.org/)
* [**Gradle plugin for schema validator**](https://github.com/alenkacz/gradle-json-validator)
* [**Computer Science Dept PUC Chile**](https://cswr.github.io/JsonSchema/)
