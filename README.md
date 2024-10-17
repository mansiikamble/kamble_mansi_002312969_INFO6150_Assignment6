"# kamble_mansi_002312969_INFO6150_Assignment6" 

**Fashion Trends - Fall 24'**

**Overview**
This repository contains the source code for a fashion magazine website, utilizing HTML and Sass/SCSS for styling. The stylesheet is organized into modular components for easier maintenance and scalability.

**HTML Structure**
The HTML code consists of:

Navbar : A responsive navigation bar
Heading : An image header with centered text
Grid Layout : It is used to make Sections for fashion trends 
Flex Box: To showcase trends from cities and their highlights
A footer : footer is added for the copyright of magazine.
table : table tag is used to give insights about brands in home page.
form : form is used to gather feedback from viewers.


**Sass/SCSS Features and Functions**

1. Variables
File: _variables.scss
Description: Variables store commonly used values like colors and font stacks, making it easy to maintain and update styles.

$primary-color: #dd376ebc;
$secondary-color: #5594b4;
etc.

2. Mixins
File: _mixin.scss
Description: Mixins allow us to create reusable blocks of CSS. The transition mixin is used for applying smooth transitions to elements.

@mixin transition($property) {
    transition: $property 0.3s ease-in-out;
}

3. Functions
File: functions.scss
Description: Custom functions enable complex calculations or conversions. The rem function converts pixel values to rem units for responsive typography.

@function rem($pixels) {
    @return $pixels / 16 * 1rem;
}

4. Nesting
Description: SCSS allows for nested styles, providing a cleaner structure by mirroring HTML hierarchy.

.table {
    th, td {
        border: 3px solid $secondary-color;
    }
    th {
        background-color: $primary-color;
    }
}

5. Placeholder Selectors
File: flex.scss
Description: Placeholder selectors (using %) are used for styles that can be reused with the @extend directive, promoting DRY principles.

%card-style {
    border: 1px solid $secondary-color;
}

6. Interpolation
Description: Interpolation allows for dynamic construction of values, useful when generating class names or other string values.

content: "Hovering over " + #{"Milan"};

8. Maps
File: style.scss
Description: Maps store related key-value pairs, making it easy to manage and retrieve complex data.

$colors: (
    primary: #dd376ebc,
    secondary: #5594b4,
);

9. Dark/Light Mode Toggle
File: style.scss
Description: This feature allows the site to switch between light and dark themes based on a variable.

$theme: light; 
body {
    background-color: if($theme == light, $bg-clr, darken($bg-clr, 20%));
}

10. Importing Partials
Description: The SCSS files are broken into partials (e.g., _navbar.scss, _grid.scss) to enhance modularity and maintainability.

@import '_variables'; 
@import '_mixin';
@import '_functions';
etc.


**Contact : For questions or feedback, feel free to reach out.**
Mansi Kamble.






