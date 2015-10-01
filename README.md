# ToFA
Update:
If you want to change icons used by jqGrid to Font-Awesome then you can have better performance by changing the style classes that jqGrid uses to generate icons, instead of changing the css. I added javascript function that overrides jqGrid styleUI icons with Font-Awesome icons which will cause all the icons created by jqGrid to be Font-Awesome icons right away. You should run the javascript function before you initialize your grid.
Note: My function will work if you use Bootstrap styleUI. If you use the default jQueryUI styles then just change the word "Bootstrap" in the script to the word "jQueryUI" and it will convert all jqGrid jQueryUI icons to Font-Awesome icons.

Old:
Easy little css that helps converting your icons to Font-Awesome icons

Inspiration for css method: @afreeland wrote on stackoverflow an idea of how to convert icons to Font-Awesome icons:
http://stackoverflow.com/questions/13862963/jqgrid-pager-area-using-font-awesome-icons/25085687#25085687

Advantages of css method:
As @afreeland stated in the link above, this method of converting icons to Font-Awesome is very fast because it uses css instead of using javascript.

Why use Font-Awesome?
Font-Awesome has much more icons than jquery-ui and bootstrap. As stated here: http://fontawesome.bootstrapcheatsheets.com/ , Font-Awesome is a library that has one purpose: give nice icons. So since this is its only purpose, it is better at that than libraries like jquery-ui and bootstrap which have many other purposes.

Note: In order for the Font-Awesome icons to really override your icons, you must give priority to the css styles in the css files here over your other icons styles. That can be achieved for example by copying the css content into a style tag in your document.

Note: The Font-Awesome unicode content css property must be inside a selector having ":before" or ":after", otherwise the icon will not appear at all.
