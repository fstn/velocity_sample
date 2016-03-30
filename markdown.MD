#set( $H = '#' )
$H  $templateTestCase.verb
#foreach( $package in $templateTestCase.getPackagesTestCase() )
$H$H $package.getName()
#foreach( $initialBlock in $package.getInitialBlock() )
```html
    $initialBlock.outerHtml()
```
#end
#end

$H$H Get Result :

```html
$templateTestCase.getResult()
```
