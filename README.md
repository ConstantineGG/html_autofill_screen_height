# autofill_screen_height
Achieve a page to automatically fill the entire screen height.
Must work for variable content height, whether that happens to be shorter or a lot longer than the screen height .

We can do this by using the bootstrap **flex** classes.

Firstly, we need to create an parent element whose height is 100% of the screen. In this example, we achieve this by:
1) giving the <html> and <body> elements "height: 100%"
2) creating a bootstrap structure (container -> row -> column) where each element is given 100% of it's parent's height, which results in the final column element to take up 100% of the screen.

**This column element is going to be our parent element.**

  Inside it, we create a \<div\> element with the classes *.d-flex* and *.flex-column* which are defined in bootstrap 4.3.
1) d-flex initiates the *flex* functionality.
2) flex-column means the the autofill will be vertical

Inside this <div>, we create our bootstrap rows that actually form our page. In this example we have:
1) a header row
2) a content row
3) a footer row

Lastly, in the content row, we give the class *flex-grow-1*. 
This makes the content row automatically expand vertically to fill it's parent, the <div class="d-flex flex-column h-100"> element, if there was not enough content to do so.
Enjoy.

~ Constantine
