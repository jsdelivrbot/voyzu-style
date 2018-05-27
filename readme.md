# voyzu-style

## Using voyzu-style

Styling contained in this component is designed to sit on top of AdminLTE https://github.com/almasaeed2010/AdminLTE (which itself sits on top of bootstrap).  

File `voyzu-style.css` contains all the css styling required.  Link to this file in your HTML page.  You will need to include a reference to the AdminLTE css stylesheet before the reference to `voyzu-style.css`

You can host the `voyzu-style.css` file yourself, for development purposes you may use the rawgit link as per the example below

Include the following  in the `<head>` tag of your html.

````html
<!-- Bootstrap -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" 
integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">

<!--AdminLTE -->
<link rel="stylesheet" href="https://rawgit.com/almasaeed2010/AdminLTE/master/dist/css/AdminLTE.css">

<!-- voyzu-style-->
<link rel="stylesheet" href="https://rawgit.com/cjlennon/voyzu-style/master/dist/css/voyzu-style.css">
````

## Local dev environment set up

1.  Clone the repo

2.  From the command line run `npm install`  This will install the `autoless` npm module which is required to build the LESS files

3.  From the command line run `npm run build`

    This will run the 'build' script contained in `package.json`.  This script will compile the less folder using the `autoless` npm module (included as a dev dependency) and move the master css (`voyzu-style.css`) to the 'dist/css' folder.

    Note that the `npm run build` script has been tested on Windows but may need modification for linux environments (uses the COPY command and escapes the slashes)

### More information (developers)

If you intend to extend or replace the `voyzu-style` styling with your own styling you may find the following information helpful

Each individual LESS file contains all the styling needed to style a component.  These components can be used accross the application.  In this way a consistant styling is achieved while still allowing modularisation of the application

The LESS files are named after the component they extend (e.g. `buttons.less` exendes the AdminLTE buttons.less file etc).