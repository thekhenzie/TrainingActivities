# Material Angular

## Install angular material and angular cdk
You can install it by typing the code below on your terminal.

```
npm install --save @angular/material @angular/cdk @angular/animations
```

## Include animations support
Import BrowserAnimationsModule in your AppModule
```js
import {BrowserAnimationsModule} from '@angular/platform-browser/animations';

@NgModule({
  ...
  imports: [BrowserAnimationsModule],
  ...
})
export class AppModule { }
```

## Import the component modules
Import the module for each component you want to use
```js
import {MatButtonModule, MatCheckboxModule} from '@angular/material';

@NgModule({
  ...
  imports: [MatButtonModule, MatCheckboxModule],
  ...
})
export class AppModule { }
```

Or better, create a separate module that imports and re-expor all the Angular Material component. 

```js
import {MatButtonModule, MatCheckboxModule} from '@angular/material';

@NgModule({
  imports: [MatButtonModule, MatCheckboxModule],
  exports: [MatButtonModule, MatCheckboxModule],
})
export class MyOwnCustomMaterialModule { }
```

Whichever approach you use, be sure to import the Angular Material modules after Angular's BrowserModule, as the import order matters for NgModules.

## Include a theme

On your global stylesheet `styles.css`:

```css
@import "~@angular/material/prebuilt-themes/indigo-pink.css";
```

## Add Material Icons (optional)
On your `index.html`

```html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
```