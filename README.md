# What's that?
Demo is hosted here, so feel free to check it out: [http://quickscad.styczen.site](http://quickscad.styczen.site)
## TL;DR version
WebSCAD attempts to provide web interface for parametrizing OpenSCAD scripts and generating STLs, gcode and renders from them.

## Long version
WebSCAD parses OpenSCAD scripts and based on the code and comments, dynamically builds an UI for parametrizing them. A doxygen-like syntax is used for describing parameters in the script. Comments may contain information about:
 - parameter name
 - parameter description
 - parameter type
 - min value
 - max value
 - accepted values (enums)
 - default values

For example, a parameter with its description may look like this:
```openscad
//@param Logo size(float) Size of the embossed image in mm
logo = 16; // [0.5:20]
```


Which tells us:  

| Property           | Value                             |
|--------------------|-----------------------------------|
| **Name:**          | Logo size                         |
| **Type:**          | float                             |
| **Description:**   | Size of the embossed image in mm  |
| **Variable name:** | logo                              |
| **Default value:** | 16                                |
| **Min value:**     | 0.5                               |
| **Max value:**     | 20                                |

# Disclaimer
This is a fun project made out of necessity, definitely not a production-grade code! I had to create a whole bunch of different keychains with different captions and symbols embossed on them, so instead af writing a bash script like any sane person, I decided to procedurally generate interfaces for every script I have in store. I did not take into account many things that should have been accounted for if this was meant to be anything more than a locally hosted rapid prototyping tool. There is a chance I will pour more time into this and properly solve performance, security and code quality issues, but as of now if you decide to host this on your server, you are on your own and have been warned.