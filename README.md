Hello! This is Zeynep :)

#### Starting the project

npm install

npm run dev

npm run test (for unit test)

In this project I'm using an API that serves cartoon characters of Rick and Morty. (892 items, cartoon characters)
I cache them into an array so we start over only when user refreshes. 

#### CSS
I have a generic file that I take from project to project, so I didn't write too much CSS for this, no worries

#### Performance
For performance I didn't make use of external libraries but used React's suspense and lazy.
And then for debouncing I made a custom function (not from lodash).
Components could be also wrapped in a memo, although they didn't unnecessarily refresh to my observation.

When I create a deep copy of the array that comes from API, I lose a bit from performance. Normally we use immer library for better performance with deep copying but I did not want to install a new library.

#### Error handling
I tried to include as many scenarios as possible. In addition to regular http errors:

- aborting in case of timeout.
- fallback page with a refresh button
- unexpected API response structure


#### Testing
Tests wasn't mentioned but I still wanted to add at least one - I also didn't install a library, I am using native Node.JS Test Runner.
but Node.js 18 or newer is needed to use the built-in test runner.

#### Accessibility
I tried to add semantic tags and aria labels for accessibility compliance.
