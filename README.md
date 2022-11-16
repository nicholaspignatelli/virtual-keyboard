# virtual-keyboard

is a keyboard that runs in browser (think like the mobile keyboard that slides up from the bottom of your screen). 


## 2022 Update

Doing something like this helps (a bit) to understand what's happening under the hood of tools like React. By directly working with the DOM API, you can begin to see the justification for why React is designed the way it is... will do a blog post on this. 
The other lesson is even if a program is small, or impractical, or can be done better in a million ways, there is still much an observant and reflective mind can takeaway. 




### Documentation
- ``` init()```: creates the elements, adds classes, adds eventlisteners, and appends children to build out the main components.
- ``` _createKeys()```: builds the keys. Adds a button element, classes, and a ruleset for handling special keys like backspace, shift, etc. the keyboard layout is hardcoded in, and really should be parameterized. 
- ``` _triggerEvent()```: generic event triggerer.
- ``` _toggleCapsLock()```: knows to caps lock only the letters (not icons) by checking if a ```key``` has any ```children```. Icons have ```<i>``` children, the letter keys have none.
- ``` open()```: triggers the opening of keyboard
- ``` close()```: 