[![Build Status](https://travis-ci.org/mezoistvan/ng2-flatpickr.svg?branch=master)](https://travis-ci.org/mezoistvan/ng2-flatpickr)

# ng2-flatpickr
ng2-flatpickr is a lightweight Angular 2+ wrapper for flatpickr, which is usable in reactive forms inside Angular.

Examples are under construction here: https://mezoistvan.github.io/angular-flatpickr-examples/.

```javascript
npm install --save ng2-flatpickr
```

Usage: import the component to the module, then declare it in order to use it in html templates.

```javascript
import { Ng2FlatpickrComponent } from 'ng2-flatpickr/ng2-flatpickr';

@NgModule({
  declarations: [
    AppComponent,
    Ng2FlatpickrComponent
    ...
```

Example usage in a form component html template:

```javascript
<ng2-flatpickr formControlName="formControlName"></ng2-flatpickr>
```

Overwrite the default flatpickr properties by inputting any of the flatpickr options: https://chmln.github.io/flatpickr/options/ 

```javascript
import { FlatpickrOptions } from 'ng2-flatpickr/ng2-flatpickr';

let exampleOptions: FlatpickrOptions = {
  defaultDate: '2017-03-15'
};

<ng2-flatpickr [config]="exampleOptions" formControlName="formControlName"></ng2-flatpickr>
```

Set a placeholder for the input:

```javascript
<ng2-flatpickr placeholder="Pick a date!" formControlName="formControlName"></ng2-flatpickr>
```

Set a date using a string or a date object:

```javascript
let randomDateString = '1988-09-19';
let randomDateObject = new Date( 1234567891011 );

<ng2-flatpickr [setDate]="randomDateString" formControlName="formControlName"></ng2-flatpickr>
<ng2-flatpickr [setDate]="randomDateObject" formControlName="formControlName"></ng2-flatpickr>

```

Flatpickr css needs to be loaded separately. when using `@angular/cli`, load it in `angular-cli.json`.

```javascript
"styles": [
  "../node_modules/flatpickr/dist/flatpickr.min.css"
]
```

TODOs until v1.0.0:
 - Meaningful tests
 - Coveralls
 - Examples with explanation
 - Closing issues
 - Rename to angular-flatpickr and deprecate ng2-flatpickr
 
