## NOTES
* currently using nested `<div>`s to render the nodes and their respective children
  * to be more semantic I should probably use an unordered list

* choices:
  * why transform data into tree vs. use the flat list?
    * I started to just use the flat list but the code to render components quickly got gross
    * both the transformation and rendering logic use recursion but it was cleaner to separate the two responsibilities
    * I *believe* it would be simpler to implement the UI in alternative ways (for example: in angular directives) if the "view layer" didn't have to worry about the initial state of the data or how it should be interpretted as a tree
  * why react?
    * It's my favorite
    * it's basically JS except for the actual rendering which uses JSX
      * no specialized controllers and directives
      * With minimal work this simple component could be transformed into other implementations since it's so close to the native web elements (JS and HTML)
    * the component tree is clear and obvious
  * I could have also done this with angular