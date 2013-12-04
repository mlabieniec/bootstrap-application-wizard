Bootstrap Application Wizard
============================

![Screenshot](http://i.imgur.com/e9B2Z.png)

General
-------
Author
* [Andrew Moffat](https://github.com/amoffat), built @ [Panopta](http://www.panopta.com/)

Contributors
* [Huzaifa Tapal](https://twitter.com/htapal)
* [Jason Abate](https://github.com/jasonabate)
* [John Zimmerman](https://github.com/johnzimmerman)
* [Shabbir Karimi](https://github.com/shabbirkarimi)
* [Gert-Jan Timmer] (https://github.com/GJRTimmer)

Dependencies
------------
* jQuery 2.x
* Bootstrap 3.x
 
Installation
------------
CSS

```html
<link href="bootstrap-wizard/bootstrap-wizard.css" rel="stylesheet" />
```

Javascript
```html
<script src="bootstrap-wizard/bootstrap-wizard.js" type="text/javascript"></script>
```

Usage
-----
#### 1) Create wizard ####

```html
<div class="wizard" id="some-wizard" data-title="Wizard Title"></div>
```

To set the title of the application wizard use the `data-title` attribute

#### 2) Create wizard cards ####
Each .wizard-card will be its own step in the Application Wizard, and the h3 tag will be used for its navigation name on the left.  Also notice the `data-cardname` attribute on each card. While not required, this can be used to access the cards by a specific name.

Card Setup
```html
<div class="wizard-card" data-cardname="card1">
    <h3>Card 1</h3>
    Some content
</div>
```


Basic Wizard Setup
```html
<div class="wizard" id="some-wizard" data-title="Wizard Title">
    <div class="wizard-card" data-cardname="card1">
        <h3>Card 1</h3>
        Some content
    </div>
    
    <div class="wizard-card" data-cardname="card2">
        <h3>Card 2</h3>
        Some content
    </div>
</div>
```

#### 3) Initialize Wizard ####
After setting up the wizard with it's cards you can initilize it.

```javascript
$(function() {
    var options = {};
    var wizard = $("#some-wizard").wizard(options);
});
```


Wizard Options
--------------
<table>
    <tr>
        <th>Name</th>
        <th>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>keyboard</td>
        <td>boolean</td>
        <td>true</td>
        <td>Closes the modal when escape key is pressed.</td>
    </tr>
    <tr>
        <td>show</td>
        <td>boolean</td>
        <td>false</td>
        <td>Shows the modal when initialized.</td>
    </tr>
    <tr>
        <td>showCancel</td>
        <td>boolean</td>
        <td>false</td>
        <td>Show cancel button when initialized.</td>
    </tr>
    <tr>
        <td>showClose</td>
        <td>boolean</td>
        <td>true</td>
        <td>Show close button when initialized</td>
    </tr>
    <tr>
        <td>progressBarCurrent</td>
        <td>boolean</td>
        <td>false</td>
        <td></td>
    </tr>
    <tr>
        <td>increateHeight</td>
        <td>integer</td>
        <td>0</td>
        <td>Deprecated</td>
    </tr>
    <tr>
        <td>width</td>
        <td>integer</td>
        <td>750</td>
        <td>Deprecated</td>
    </tr>
    <tr>
        <td>contentHeight</td>
        <td>integer</td>
        <td>300</td>
        <td>Default height of content view</td>
    </tr>
    <tr>
        <td>contentWidth</td>
        <td>integer</td>
        <td>580</td>
        <td>Default width of wizard</td>
    </tr>
    <tr>
        <td>buttons</td>
        <td>array</td>
        <td>
            cancelText: "Cancel",<br />
            nextText: "Next",<br />
            backText: "Back",<br />
            submitText: "Submit",<br />
            submittingText: "Submitting..."<br />
        </td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>

Logging can be turned on by setting logging setting before wizard initialization
```javascript
$.fn.wizard.logging = true;
```


To be Removed
# [Demo & Complete Documentation](http://www.panopta.com/2013/02/06/bootstrap-application-wizard/)
