# Managing the Fullstack Application

1. Describe the two ways to bind Data in Vue?

  > | One-Way Data Binding: One-way data binding allows you to bind data from the component's JavaScript code to the template (view). Any changes in the JavaScript data will automatically reflect in the template, but not vice versa. via {{ }} brackets 
  
  Two-Way Data Binding: Two-way data binding allows you to bind data from the component to the template, as well as from the template to the component. This means that changes made in the template will update the component's data, and changes made in the component's JavaScript code will update the template. Two-way data binding is commonly used with form inputs and is achieved using the v-model directive|

2. The `SPA` acronym stands for what?

  > | Single page application |

3. What are some of the advantages/uses of a `SPA` over a traditional one?

  > | Enhanced User Experience: SPAs provide a more fluid and responsive user experience. Since SPAs load all the necessary code, assets, and data upfront, interactions feel faster. Seamless Navigation: SPAs enable seamless navigation between different sections or views within the application without the need for full page reloads. |

4. What does the `onMounted` method in Vue do?

  > | OnMounted is used to execute code when a component is mounted onto the DOM |

5. What is the `v-model` attribute in Vue for, and when might you use it?

  > | The v-model directive in Vue is used for two-way data binding between form input elements and component data. |

6. What is the package.json file used for?

  > | Dependency Management, Script Definitions, Configuration Settings, Project Initialization  |

7. Which Vue attributes(directives) could you use to conditionally render elements on a page?

  > | v-if directive v-else-if, v-else, v-show |

8. What is the purpose of the `key` attribute when using `v-for` on an element?

  > | It helps Vue efficiently identify and track the individual elements within the list. The key attribute provides a unique identifier for each rendered item in the v-for loop. |

9. What is the `<slot>` element and what is it used for?

  > | <slot>  allows you to define placeholders for content within a component's template. It provides a way to pass content from the parent component into the child component. |
