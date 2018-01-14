# CSS Playground

This is my CSS playground for re-learning and messing around with CSS concepts. This is also a place for me to keep notes on things I didn't know or don't want to forget.

Divs:
    Default for divs is to take 100% of its container minus padding/margin in Box model.
    When you give a size in percentage it is of its container
    As long as you have a <div> with a certain width you can use auto to center a div horizontally.

Margin/Padding order = T R B L (Clockwise)
Margin is outside
By Default Padding adds to width and height of Element
Padding is the space between the content and border (inside)

Selectors:
    [element] [element]	| div p | Selects all <p> elements inside <div> elements
    [selector_1] > [selector_2] The > combinator selects nodes that are direct children of the first element.
        e.g: ul > li will match all <li> elements that are nested directly inside a <ul> element.
    
min-height: Give an element a nice default height but will allow growth incase of big content

Display Elements:
    display: block = Takes up entire width of something usually its parent. Headings(h1-hX) and Paragraphs tags block by default
    display: inline = Take up the amount of space it needs to take up and cannot have set heights and widths. Spans and anchor links are inline by default
    display: inline-block = Takes best of both worlds, It is inline but can be given height and width.
    display: none = Hides element and the space it would have occupied 
    visibility: none = Hides element but leaves space that it would have taken up there.

