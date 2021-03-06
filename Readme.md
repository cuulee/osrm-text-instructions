# osrm-text-instructions.js

----

__WIP: This project is under heavy development and should not be integrated yet.__

osrm-text-instructions.js is a library to transform OSRM steps into text instructions.

### Usage

```
var osrmTextInstructions = require('osrm-text-instructions')('v5');

// make your request against the API

response.legs.forEach(function(leg) {
  leg.steps.forEach(function(step) {
    instruction = osrmTextInstructions.compile(step)
  });
});
```

### Design goals

- __Cross platform__ Use a translation table in JSON and short logic to allow easy implementations in other languages
- __Heavily tests__ We have a data-driven test suite with fixtures which can be used cross-platform
- __Customization__ Users should be able to easily fork or monkey patch the results to adjust to their own likings
- __Translation__ Allow for translations via [Transifex](https://www.transifex.com/)
