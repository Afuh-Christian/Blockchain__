
# solidity . 
 staticly typed  


 - Begin smart contracts files names with capital letters . 
# Contracts 
    - supports inheritances 
    - object-oriented   
 
# Variables 
 - State : within solidity contract 
 - Local : within solidity function 

# Types 

### uint 
    - unsigned interger . 
    - can't be negative 


# declaring a function 

```html

 function <functionName>(<parameter>) <visibility> <editability> return(<returnType>){

    return ...
 }

```


# View vs Pure Functions 

####  view 
```Read-Only```: view functions can read state variables but cannot modify them.
```State-Dependent```: They can access and return values of state variables.
```No Gas Cost```: Calling a view function externally does not cost gas if it is called locally, but it does cost gas if it's called within a transaction.

#### pure

```No State Access```: pure functions cannot read or modify state variables.
```Computation Only```: They can only use parameters passed to them and local variables.
```No Gas Cost```: Similar to view functions, calling a pure function externally does not cost gas if called locally, but it does cost gas if called within a transaction.


# Default size for unsigned intergers in solidity  ==== 256 bytes .  





# Array .  
To get the array after deployment .  
  - get the size 
  - you'll be prompted to input the index of the element you want . 



# functions with parameters . 


In Solidity, when you create a function that receives parameters, especially if they are complex data types like arrays or structs, you typically need to specify where these parameters will be stored. The two main places are memory and storage.

### memory vs storage in Solidity:
##### Memory:

Parameters declared as memory are temporary and exist only for the duration of a function's execution.
Use memory for parameters that are passed to functions and are not stored on the blockchain.
Solidity automatically manages memory for you when you declare function parameters as memory.


```js
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Arrays {

    string[] public values;

    function addValue(string memory _value) public {
        values.push(_value);
    }

}


```

##### Storage:

Variables declared outside functions or as state variables in contracts are stored in storage.
storage refers to the persistent storage on the Ethereum blockchain.
Use storage when you want to persist data across multiple function calls or transactions.




