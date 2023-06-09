**Gregslist Node** - Publish to github immediatly 
* first step is update .env in server workspace and then do the same in client workspace.
* Make sure when you using bcw you are starting it from the Client Folder
* schema is the same as class for the DB
* Import Mongoose to use as a translator for the javascript model and teh datbase schema
* `cars.js`
* `import mongoose from mongoose`
* `const schema = mongoose.schema`
* `export const CarSchema = new Schema(
  {
    model:{type: String, required: true}
  }
)`
* **register the schema** - in the folder db-->DbContext.js - here is where we register schemas similar to what we did for controllers on the client side
* `Cars = mongoose.model('Car', CarSchema)` 
* `DbContext` is the server side version of appstate. access with `dbcontext.cars`

* **

* **Step 1** create model **Step 2** register model/schema in DbContext then you can begin to code
* **Step 3** create controller & service to interact with your new model extend newcontroller to BaseController via inheritance
* whe posting new data we will use the `.Create(newData)` method from mongoose to create 
* when doing n edit we need to do whats called a `null check` check to see the id passed exists
* **
* **key concepts**
  * schema / server side model
  * ObjectId
  * Inheritance
  * Mongoose and its methods
  *  