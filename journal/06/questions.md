# Single Page Applications with Vue
01. What is the entrypoint of an application?

  > | The entrypoint of an application in Vue is the file that is responsible for loading and initializing the Vue application. In a Vue CLI app, the entrypoint is typically the main.js file. This file is responsible for importing all of the necessary Vue components and libraries, and then creating and initializing the Vue application. also the Viewport |

02. What is the difference between a vue `component` and `page`?

  > | 
In Vue, a component is a reusable piece of code that can be used to create a specific UI element or functionality. A page, on the other hand, is a complete Vue application that consists of multiple components.  |

03. What is ***Component-Based Architecture***?

  > | Component-Based Architecture (CBA) is a software development approach that breaks down a software application into smaller, reusable components. These components can be independently developed, tested, and deployed. CBA can help to improve software quality, maintainability, and flexibility. |

04. What are the three tags that make up a Vue component?

  > | Template, script, style |

05. What are ***lifecycle hooks***? What are lifecycle hooks used for?

  > | Lifecycle hooks are special methods that are called at specific points in the lifetime of a Vue component. They can be used to perform tasks such as initializing data, mounting the component to the DOM, and updating the component's state.|

06. Which component in Vue does the vue-router use to mount pages onto?

  > | Vue-router uses the router-view component to mount pages onto. The router-view component is a special component that is used to render the component that is associated with the current route. |

07. What is the difference between the `AppState` and the state object within a component?

  > | AppState is a global state object that is shared by all components in an application. It is used to store data that is common to all components, such as the current user, the current page, and the current settings. |

08. What is the responsibility of `Services` in our Vue projects?

  > | We use services whenever vue needs to manipulate data |

09. What are ***props*** and how are they used? Provide an example

  > | Props are data that is passed from a parent component to a child component. They are used to provide data to the child component and to control the behavior of the child component. |

10. What is the Vue method used to create watchable objects such as `state` or `AppState`?

  > | watch() is a method that is used to create watchers. Watchers are functions that are called whenever the value of a property changes. This can be used to update the UI, perform actions, or log data.|
