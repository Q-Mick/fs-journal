# Intro to JavaScript
01. Which keywords are used to declare a variable in JavaScript?

    > | let, var, const |

02. What is the definition of a function?

    > | a function is a *subprogram* designed to perform a particular task and are only executed when we call them, aka invoking them. |

03. What are the `SOLID` principles?

    > | S - single responsibility | O - open-closed-principal | L - Liskov Substitution principal | I - Integration Segregation Principle | D - Dependency inversion Principal


04. Given this array: How could you remove the `pineapple`?

    ```js
    let fruit = ['apple', 'banana', 'pineapple', 'orange', 'strawberry']
    fruit = fruit.splice(2, 2)
    console.log(fruit)

    ```

    > | fruit.splice(2, 2) |

05. Given these two objects: How could you add each to the others friends arrays?

    ```js
    let you = {
        name: "You",
        hair: true,
        friends: []
    }
    let them = {
        name: "Them",
        hair: false,
        friends: []
    }
    ```

    > | you.friends = them.friends.concat(you.friends) | them.friends = you.friends.concat(them.friends)

06. Give an example of a JavaScript `Conditional`:

    > | if(thisIsMyJournal == true) |

07. What is the main difference between `parameters` and `arguments`?

    > | parameters are the what tell you what arguments the function is asking for and the argument is the data itself  |

08. Instead of writing everything to the console, what is a better way to debug your code?

    > | debugger keyword |

09. What is the difference between a `primitive` value and a `reference` value?

    > | a primitive value is a simple data type that is not an object and has no methods. Primitive values include basic data types such as numbers (integers, floats, etc.), Booleans, and characters.|

10. Demonstrate a loop that prints the numbers between -100 and 100?

    > | for (let i = -100; i <= 100; i++) {
  console.log(i);
} |
