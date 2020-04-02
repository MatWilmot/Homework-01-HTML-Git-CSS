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

## Notes
- The ```search-engine-optimization``` article was missing an ```id=""``` element in its opening tag. I added one.

- The ```Cost Management```'s ```<img>``` tag had a ```</img>``` after it. This isn't necessary, so I removed it.

- The CSS file was addressing multiple different classes with identical parameters:
  - ```.benefit-lead```, ```.benefit-brand```, and ```.benefit-cost``` all apply the same **margin** and **color**.

  - ```.benefit-lead h3```, ```.benefit-brand h3```, and ```.benefit-cost h3``` all apply the same **margin** and **text-align**.

  - ```.benefit-lead img```, ```.benefit-brand img```, and ```.benefit-cost img``` all apply the same **display**, **margin**, and **max-width** values.

  - ```.search-engine-optimization```, ```.online-reputation-management```, and ```.social-media-marketing``` all apply identical values.

  - ```.search-engine-optimization img```, ```.online-reputation-management img```, and ```.social-media-marketing img``` all apply the same **max-height** value.

  - ```.search-engine-optimization h2```, ```.online-reputation-management h2```, and ```.social-media-marketing h2``` all apply the same **margin-bottom** and **font-size** values.

  - *I created a new class for ```benefit-lead, benefit-brand, and benefit-cost``` called ```benefits``` and replaced all code reliant on those classes, reducing 9 class rules down to 3.*
    
    *Similarly, I replaced ```search-engine-optimization, online-reputation-management, and social-media-marketing``` with a new class called ```article-format``` and replaced all code reliant on those classes, reducing 9 class rules down to 3.*

- The CSS file was not addressing the HTML elements in the order they occurred, I cut and pasted segments of the CSS file to fix this.