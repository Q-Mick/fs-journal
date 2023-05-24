**models**
 * `import mongoose from "mongoose"`
 * `const Schema = mongoose.Schema;`
 * when declaring the Object ID in the model it looks like this and you must specify the reference if it used another model to reference. 
 * `SchoolId: {type:schema..types.objectid, required: true, ref: 'school'}`
  * register in db
  * create controller and service js files
    * code `constructor()`
    * code `super(api/path)`
    *  `this.router`
    * code the `create()` function and make a new ---> `dbcontext.Schools.create`
    * use postman to validate that it works then finish creating routes

**Virtuals**
  * `CourseSchema.virtual('school',{localfield: 'schoolId, ref: 'school', foreignField: '_id', justOne:true})`

  * **
**ONE TO ONE**
  * ref is one other model ID
  * make sure to use populate() in these

**ONE TO MANY**
  * ref is two other objectIds
  * must use virtuals
  * supply one side of the relationship and return the other
  * typically you are supplying the parent ID to get its inner properties

  **MANY TO MANY**