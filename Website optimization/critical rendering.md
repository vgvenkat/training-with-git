#Critical Rendering Path
The steps browser takes to convert HTML, CSS, Javascript to pixels on the page.

**Steps**
- Fetch HTML for DOM
- Fetch CSS for CSSOM
- Combine both for the render tree
- Where everything goes? Layout step
- Then pixels on screen

How does HTML get converted into DOM?
Browser has a tokenizr that reads <html> with a start tag html and </html> with end tag html, this helps in drawing relationships between. This draws a tree.

Incremental HTML delivery,
Flushing - send the common elements like header, footer early even before the search queries appear.

### Using timeline in chrome dev tools
- start testing performance issues in the timeline panel.
