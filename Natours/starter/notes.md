    responsive design - works the same across all devices
    maintainable and scalable code - write code that is clean and easier to understand that is reusable
    web perfmance - making it faster and smaller in size. small http requests as possible

    **How CSS values are processed
        1. declared value - author declarations
        2. cascaded value - after the cascade
        3. specified value - defaulting, if their is no cascaded value
        4. computed value - converting relative values to absolute
        5. used value - final calculations, based on layout
        6. actual value - browser and device restrictions

    rem values are always relative to the root 

    when dealing with percentages - 
        - a font percentage will give you a font that is the specified percentage bigger than the parent font. [ parent = 100 font-size = 10% => 110 ]
        - a percentage for lengths or anything else, will give you the specified percentage of the parent element. [ parent = 100 padding = 10% => 10 ]
    
    em and rem are font-based units
    em uses parent or current element as reference
        em for fonts references the parent element
        em forlengths reference the current element
    rem uses the root font size as the reference
    * because these are based on font sizes, when the font size changes so everything sized with REM and EM

    vh and vw are based on the browsers viewport
        vh - 1:1% viewport's height
        vw - 1:1% viewport's width

    root font size is changed in the html selector




sass = preprocessor for css

sass source code ->sass compiler-> compiled css code

variables
nesting - nest selectors inside one another
operators - for mathematical operations inside of css
partials and imports - allows us to write css code in different files and import them into a single file
mixins - write reusable pieces of css code
functions - like mixins, but produce a value that can be reused
extends - dif selectors inherit declarations that are common to all of them
control directives - for writing complex code using conditionals and loops 


two types of syntax - sass and scss

sass - indents and no curly braces
scss - preserves the way original css looks

variables defined with '$'
    $color-primary: #fff
variables can be used throughout the file.

nesting selectors:
    .navigation {
        list-style: none

        li{
            display: inline-block
        }
    }
there is no limit with how far you can nest
& within a nest == the nest up until that point

using mixins
    declare:
        @mixin mixin-var-name {
            some css 
        }
    use:
        @include maxin-var-name
you can also pass in arguments to mixins and treat it like a function. 
    declare:
        @mixin style-text($text-color) {
            text-aline: center;
            color: $text-color
        }
    use
        @include style-text(red)
this is useful for when you want to make your code dry, but some styles may vary

extends should only be used for properties that re actualy related to one another. 

scss files beginning with "_" are partial files that will be used to compile into the main scss file 
to import into main.scss:
    -- @import "file location"
        you dont have to write the "_" or .scss on your import

        7-1 architecture
main.scss should only hold imports
base files are partial files that will hold the base of the css - basic definitions of our project
abstracts file will hold all of the code that does not output css (variables, mixins, etc)
components
layouts
pages


responsive design principles:
fluid grids: allows content to easily adapt to the current viewport width
    - use percentages for all layout related lengths

flexible and responsive images: they do not scale automatically to the current view port so we have to make sure we account for this by defining their dimensions in percentages instead of pixels

media queries: allows us to change styles on certain viewport widths, allowing us to create different versions of our website for different widths


layout types:
float based layouts: place boxes side by side. 
flexbox: 
css grid: 


