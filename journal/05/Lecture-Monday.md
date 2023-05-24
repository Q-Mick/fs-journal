**node and EXPRESS INTRO**
* services will match the services on our backend.
* database never talks to the front end.
* We will use postman to fake the front end requests.

**IMPORTANT**
* **command to install dependencies** - be in the same directory as package.json then run NPM i


**EXPRESS JS** mondays lecture
* **client** folder has an index.html only - will touch back later
* **package.json** Is the single most important thing to learn right now
* **dependencies** - **express** - cors - dotenv - esm - helmet - mongoose - socket.io
* **Express** - Is the backbone of all of this.
* **Mongoose** - Will be used to talk to our database.
* **socket.io** - Can be used for communication on the site
* **index.js** in order to run .js files we use the node command
* **npm init -f** creates the package.json with a script section and inut **"node index.js"** hitting the play button will initiate via the package.
* **.env** - Needs to be configured before being able to communicate directly with the server - Follow this to the **main.js**
* feel free to use the sandbox config today for our auth0 authentication verify **localhost:3000** works then add **/api/values**

* **BaseController** is the main controller and any declared controller has to **extends** to the base controller
* **constructor() and super('api/path/')** - these are the setups
* **this.router** - .get, .post, .use, - this is used to setup the code that triggers as these requests come in from the client
* **changes to server - respin** - if you add a value don't forget to respin the server
* **req.params.id** - .id is based on the /:id path - so it basically becomes your variable to access it via dot notation
* **
**Lets write our own**
* Create a Tiger controller - `export class TigersController extends BaseController`
  * **create the constructor and super** - 
  * `Constructor()
    * Super('api/tigers)`
  * **this.router** - prepare any gets, posts and functions. Make sure to send a response back.
  * .get(' ', getTigers)`
  * async getTigers(req, res, next)
    * res.send('🐅') <---This is the response going back
* **
**Create service and create get and return correct data**
* Use logger.log('Message to log') instead of console
* db will hold out data
* create Tigers service `export const tigersService = new TigersService`
* create getTigers() return fakedb.tigers
* These commands communicating with the db will be async so use `async` and `await`
* create a handler for id via `.get(/:id', this.getTiger)`
* logger.log `req.params.id` always look in the debugger to see the correct path if you are unsure of the data you are looking for.
* **create** - `getTigerById('req.params.tigerid')`
* `const tiger = FakeDb.tigers.find(t => t.id == tigerId)`
* **return error if no tigerID** - ` throw new BadRequest('invalid tiger id')`
* **return tiger** - `res.send(tiger)
* **
**Next we will write some put methods**
* **In constructor add** `this.put('/:tigerID')`
* **check data sent in** `req.body` to see what was sent to us in the put request.
* **write the code for the function to update tiger** - `editTiger(updateTigerData)`
  * `tiger.name = updateTigerData.name || tiger.name`
  * `tiger.picture = updateTigerData.picture || tiger.`picture
  * `res.send(tiger)`
* **
**PUTS AND DELETE**
  * **BODY** - gets and deletes dont have .body puts and post do* data will be in req.body
  * we `push` the data in to an array via `push`
  * Don't allow for the same ID so make sure you generate an ID if one is not provided and make sure its not the same as any other tigers in your db.
* `make sure to register all of these endpoints in the router`