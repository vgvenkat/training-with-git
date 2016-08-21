### SMACSS
- Naming convention is really important for scalable css.Helps find if components go together or not.
- Decouple css from HTML
- State based design.
aside: use modules in scss
#### Writing CSS
**Base**
- Write a base CSS with just element selectors. i.e. using html, body, h1,h2 setting default padding, width
- check : if adding resets has really any change after writing styles.

**Layout**
- Check how you group content, header, side bar, content and how grid systems would apply.

**Modules**
- These are the customized tabs, list views and buttons. Contain content.
- *Sub-Modules* moduels that are different in a small way. Like different types of buttons i.e. different sizes, colors with/out images.

**Consolidation**
- if there are a number of dropdowns with subtle variations, check if the dropdowns can be grouped.

**State**
- What happens when modules are interacted with, button state on click, hover.

**Theme**
- if elements are isolated and need different colors and themes happen.
