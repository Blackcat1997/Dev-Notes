# JavaScript

## Data type

### 📖 How many data type are there in the JavaScript?

- **Seven (Two kinds)**

  - In JavaScript there are two different kinds of data: **Primitive** and **Objects**.

  - Primitive: it's no a object and has no methods

    - Number
    - String
    - Boolean
    - Null: has a value
    - Undefined: no value
    - Symbol: immutable value, means it's a constant

  - Objects: a collection of properties

    ```JavaScript
    var obj = {
      key1: value1,
      key2: value2,
      key3: value3,
      ...
    }
    ```

### 📖 Why is String a primitive type but it has methods?

When calling string methods, the string value will be coerced into a the string value will be coerced into a string object in order to access the `length` method. In other words, JavaScript will actually temporarily convert the primitive string value into an object so it’s able to use the `.length` method property up in the prototype chain.

