**Thursday lab**

* NASA API - potd that we can save favorites - aka more api practice.
* api.nasa.gov- this is the link to nasas api
* **STEP** 1 - start by settig up env.js for the codeworks sandbox

* **STEP** 2 - create NASA controller --> make constructor  -- > set it up in Router.js and add the controller to the home path array.

* **STEP** 3 - Go look at the NASA API and check the documentation to verify endpoints and get insight in to how the nasa api works

* **STEP** 4 - Setup NASA API instance in Axios to be able to query the nasa api. BaseURL:api.nasa.gov - Timeout:8000 - params{api_key: _'keyhere'_} you will have to signup for a key if you want to use this

* **STEP** 5 - create async **getPictureOfTheDay()** in controller and send it to the **NasaService--->** create service file

* **STEP** 6 - async getPictureOfTheDay(){ const res = await nasaapi.get(re)}

* **STEP** 7 - after getting the data create a model to map that data into.

* **STEP** 8 - make sure to include all of the relevant data that you want to store in the model.

* **STEP** 9 - put the incoming data in to a new instance of our model **AppState.ModelName = new Model(res.data)**

* **STEP** 10 - Now that we have the data with a picture url lets draw data on to the background `const picture = AppState.picture, document.body.style.backgroundimage=url(${picture.image})` make sure to add an appstate.on for the data to be loaded in to memory before we try to access it and draw.

* **STEP** 11 - we have the information now we need to create a template in our model to display in our _draw function

* **STEP** 12 - look at todays lab for the visible on hover css tip and making a blur behind the text to make it easy to read depending on the background.

* **STEP** 13 - give the id to an html element so we have a place to inject our html. Create getter in model

* **STEP** 14 - make an input to accept a date so we can pull a specific days picture. `input type="date" class="form-control" name="date" id="date" onchange="app.Controller.selectDate()"` make that function
* **STEP** 15 - create function in the controller use try catch and send to service
* **STEP** 16 - get the date html element and then store the value and log it to check the date - query nasa api and send that date selectDate(date) `?date=${date}` if logs are correct store the data in a new instance of our class and update screen via the listener on the object. we are done with the nasa api now we move to sandbox api.
* **STEP** 17 - create sandboxapi controller and service - `add sandbox controller we created to the router`
* **STEP** 18 - at this point we do a create favorite function in the sandbox function `sandboxService.favoritePicture(favoriteData)` in controller do a let favoritePicture = appstate.nasaPicture  api.post()

* **STEP** 19 - Work through the network errors in the post() and update model structure to work with the structure required.

* **STEP** 20 - reference post function `favoritePicture()` in sandboxService to sork through this problem

* **STEP** 21 - get favorites from the sandbox server via getFavorites() using aapi.get(`api/apods`) -->

* **STEP** 22 - draw favorites in the 

* **STEP** 23 - create delete favorite then setup function to remove favorite from sandbox server

* **STEP** 24 - removeFavorite(id) `await sanboxapi.delete(id)`
* **STEP** 25 - after removing and confirming we need to delete it from appstate/local memory array 
* **STEP** 26 - celebrate with a beer