# CSharp and SQL Fundamentals
01. What is the purpose of a `namespace`?

  > | A namespace in C# serves as a container or a grouping mechanism for organizing related code elements. It acts as a virtual boundary that separates different sections of your codebase, preventing naming clashes and promoting better code organization. |

02. What is the difference between a `class` and an `interface`?

  > | A class is a blueprint for creating objects. It defines the data and behavior of an object where an interface defines a set of methods or behavior that a class should follow |

03. What is the method that returns an instance of a class, yet it has no return type?

  > | That would be the special method called a constructor, its responsible for initializing new instances of a class. Its purprse is to create the instance rather than return a value. |

05. In the Car example what is the access modifier of the `Start()` method?

  ```c#
  abstract class Car
  {
    public string Start()
    {

      return "Vroooom";

    }
  }
  ```

  > | the public access modifier allows the method to be accessed from the entire codebase, even other classes, it can be invoked by any code that has access to an instance of Car. |

06. In the Car example what is `string` an indication of?

  > | string would be the expected return data type when triggereing the Start method. the method returns the string "Vroooom" |

07. In the Car example what is `abstract` preventing?

  > | marking a class as abstract is saying the class is meant to serve as a base or blueprint for other derived classes, it can not be instantiated as-is|

08. In a SQL table, what is the difference between information in a row and information in a column?

  > | ANSWER HERE |

09. Demonstrate the necessary SQL for creating a table called `characters` with the values `name, age, description` as strings, and an `int` id.

  > | Arows hold a complete set of related data for the entry where columns only contain a specific type of data or individual attribute ie: Cars.make would be a column and a row would contain all of the cars values(make, model, year, price, id, etc)|

10. In SQL how can you query more than a single table? Provide an example.

  > | You can use the JOIN command
  string sql = @"
    INSERT INTO recipes
    (title, instructions, img, category, creatorId)
    VALUES
    (@title, @instructions, @img, @category, @creatorId);

    SELECT
        recipe.*,
        creator.*
    FROM recipes recipe
    JOIN accounts creator ON recipe.creatorId = creator.id
    WHERE recipe.id = LAST_INSERT_ID()
    ;"; |
