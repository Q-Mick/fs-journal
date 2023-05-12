# MVC

**MVCS design principals**

**MVCS** model, view, controller, service
* the industry standard for code organization


**VIEW**
* html dom, index .html, html representation of the data in the app

**CONTROLLER**
* takes in actions from user, draws data to dom
* it is never the job of the controller to handle data manipulation. That is the job of service
* controllers are like the 'filter' layer between the users inputs and the rest of the app
* anything the the user can interact with will come through the controller first
* all controllers need registered in the app.js
* observers go in constructors add an .on(var_here, function_to_call) to listen
* appstate.emit(players) will trigger the observer/ .on for this class

**SERVICE**
* business logic happens here. anything that modifies data(appstate) goes here


**APPSTATE**
* single source of truth aka where all the app's data will be stored

* the DATA or new instances of classes are stored here

**MODEL**
* Blueprint of what the data in the appstate will look like



**singleton pattern**
* singleton says there is only ever one of these created
* export const heroesService = new heroesService()

** appState.emit('heroes') will trigger the listeners to realize the object has changed