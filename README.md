# Landing Strip
- Put all possible additions, questions, and changes being contemplated here.
- Minimization on build (instead of dev).  Put into a new, seperate folder?
- Explain sub-scss folders/files.
- Add grid file.
- Use Bower to install JQuery and FontAwesome and all that jazz.  But 'base' shouldn't include these as every project might not use them.  So only remark that it is possible with bower and that is why it is installed.   Include Modernizr and Normalize?
- Should Bower install somewhere other than outside the "app" directory?


# Preperation
- Copy base folder to new project location.
- Change folder name to new project name.
- Enter new project settings into "package.json" file.
- Install Ruby on machine.
- Install Node.JS on machine.
- Install Git on machine, select option to run from Windows CMD.

*I recommend using PowerShell for the rest.*
- Run "npm install -g bower".
- Run "npm install -g grunt-cli".
- Run "npm install grunt-contrib-sass --save-dev".
- Run "npm install grunt-contrib-watch --save-dev"

# To Run
Run "grunt".

# Technologies Used
- Node.js
- Grunt
- grunt-contrib-sass
- grunt-contrib-watch

# File Structure Breakdown

## base #######################################################################
- The root of the project.  The only folder in this directory that will be uploaded is the "app" folder.  All other files and folders are simply to assist in the development of the site, but are not part of the site itself.

### app
- The only folder in its directory that will be uploaded.  Contains the actual site.

### docs
- Contains any documentation for the site.

### node_modules
- Auto-generated folder that contains installed modules used to assist in the site development.

### src
- Contains raw files that will be manipulated in some way and then put in the "app" folder.  Includes .SCSS files, .JS files, and images.  For example, this folder takes raw .SCSS files and converts/minimizes them into .CSS files and puts them into the appropriate folder in the "app" directory.

### Gruntfile.js
- What Grunt uses to handle its tasks.

### package.json
- What Node and Grunt use for project identification.  They can pull information, such as the project title or author, and insert them into files when needed.

### bower_components
- Where Bower puts the components you choose to install.

### .sass-cache
- Auto-generated folder upon compiling SASS.  You can ignore this folder.


## base / app #################################################################
- Description above.

### assets
- Contains site-ready .CSS, .JS, fonts, and image files. 

### .htaccess
- The .htaccess file helps control the incoming URLs.


## base / src #################################################################

### img
- Contains the raw, uncompressed images.

### js
- Contains unminimized .JS files.


## base / src / scss ##########################################################

### mixins
- SCSS mixins

### modules
- Contains the styling for the different elements that websites are composed of.  Inputs, typography.  Mainly predefined elements, not classes or ids.

### pages
- Contains the styling for each individual page.  Starts with the basic index.scss for the initial home page.

### partials
- Contain the different sections of the site such as the header, footer, and nav.

### vendor
- Contains vendor scss.

### style.scss
- The main style sheet that all .SCSS files located in this directory will compile into, EXCEPT the pages subdirectory, because you do not want to load all of the CSS for every single page at once.  Load it when the user goes to that specific page.