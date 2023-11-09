## Reproduction

### [package.json](package.json)
```json
...
"dependencies": {
  ...
  "@angular/material": "^17.0.0",
  "@shared/styles": "file:./src/shared/styles",
  ...
}
...
```
**Note:** *Bug is not related to @angular/material.
It's only included to demonstrate that actual packages are not affected.*

### [src/styles.scss](src/styles.scss)
````scss
@use "@angular/material";        // this one works fine
@use "@shared/styles/functions"; // this one breaks the build
````

### [src/shared/styles/functions.scss](src/shared/styles/functions.scss)
````scss
// exists
````
