[WARNING]
This repo is a copy of what was originally here: https://github.com/magento/marketplace-tools

Seems that it has been abandoned. But I use it to validate extension zip for Marketplace submission.

# Marketplace tools
The idea behind this directory is to house standalone tools that developers can use to validate/verify their extensions before submitting them to the Marketplace. Currently, it only houses a package validation tool for Magento 2 Extensions. In the works is a standalone tool that will generate a CodeSniffer report for a given Extension.
###### validate_m2_package.php
```
Usage: validate_m2_package [OPTIONS] <M2 zip file> [<M2 zip file> ...]

       -h  help
           Prints this usage.

       -d debug
           Optional - prints additional debug messages.
```
The tool is silent on success unless the debug option is set. If the tool finds any errors it will report them in the following format to make the errors searchable:

ERROR - "\<zip file name\>": Error message.

Errors must be fixed, warnings and notes are purely informational. The user can fix any warnings or notes but is not required to.
