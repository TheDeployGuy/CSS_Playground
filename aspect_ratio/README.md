# Aspect Ratio

If you have ever done web development before you have seen the issue where you have text that loads in before an image and it causes a jump in the page. There were various ways / hacks to get around this, setting heights for initial load (via ::before pseudoselector or via a div). In 2019 there is now a better way to do this via CSS.

All you need to do is have a height:auto on your image selector and a width and height set in your image tag. When the browser sees height:auto, it will take the values specified in the image tag and set the width and height accordingly. Now when you load the page there is the perfect amount of space for your image to load! no more jumping text!

https://youtu.be/eCGW0FKZ1gg?t=194
