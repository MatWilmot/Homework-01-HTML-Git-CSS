# 01 HTML CSS Git: Code Refactor
## Acceptance Criteria:
```
GIVEN a webpage meets accessibility standards

WHEN I view the source code
THEN I find semantic HTML elements

WHEN I view the structure of the HTML elements
THEN I find that the elements follow a logical structure independent of styling and positioning

WHEN I view the image elements
THEN I find accessible alt attributes

WHEN I view the heading attributes
THEN they fall in sequential order

WHEN I view the title element
THEN I find a concise, descriptive title
```

## Action Plan
1. Carefully read through the index.html file to get a feel for the code I'll be working with. 

2. Go through each ```<div>``` element and determine whether or not it requires updating to conform to new HTML semantics.

3. As I update each ```<div>``` element, also update the corresponding classes in CSS for those divs to reflect the new element and not break the code.

4. Go through each ```<img>``` tag and add an ```alt=""``` attribute to make the page more accessible to visually impaired people.

5. Re-word the ```<title>``` element to give the page a more relevant title.

### Notes
The ```search-engine-optimization``` article was missing an ```id=""``` element in its opening tag. I added one.

