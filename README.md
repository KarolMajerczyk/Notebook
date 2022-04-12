# Notebook

FreeCodeCamp Notes

## Responsive Web Design Certification

<details><summary>Basic HTML and HTML5</summary>

HTML is a markup language that uses a special syntax or notation to describe the structure of a webpage to the browser. HTML elements usually have opening and closing tags that surround and give meaning to content. For example, different elements can describe text as a heading, paragraph, or list item. HTML elements are the building blocks of any webpage.

Most HTML elements have an opening tag and a closing tag. The only difference between opening and closing tags is the forward slash after the opening bracket of a closing tag.

For example this is a heading element with opening and closing tag:

```html
<h1>Main heading element</h1>
```

Heading element tells the browser about the structure of your website. h1 elements are often used for main headings, while h2 elements are generally used for subheadings. There are also h3, h4, h5 and h6 elements to indicate different levels of subheadings.

```html
<h2>2-level heading element</h2>
<h3>3-level heading element</h3>
<h4>4-level heading element</h4>
<h5>5-level heading element</h5>
<h6>6-level heading element</h6>
```

The p element is the preferred element for paragraph text on websites. p is short for "paragraph".

```html
<p>Paragraph element</p>
```

Note: As a convention, all HTML tags are written in lowercase.

Web developers traditionally use lorem ipsum text as placeholder text. The lorem ipsum text is randomly scraped from a famous passage by Cicero of Ancient Rome. Lorem ipsum text has been used as placeholder text by typesetters since the 16th century, and this tradition continues on the web.

Commenting is a way that you can leave comments for other developers within your code without affecting the resulting output that is displayed to the end user. Commenting is also a convenient way to make code inactive without having to delete it entirely.

```html
<!-- HTML comment -->
```

HTML5 introduces more descriptive HTML tags. These include main, header, footer, nav, video, article, section and others.

These tags give a descriptive structure to your HTML, make your HTML easier to read, and help with Search Engine Optimization (SEO) and accessibility. The main HTML5 tag helps search engines and other developers find the main content of your page.

```html
<main>
  <h1>Hello World</h1>
  <p>Hello Paragraph</p>
</main>
```

You can add images to your website by using the img element, and point to a specific image's URL using the src attribute. Note that img elements are self-closing. All img elements must have an alt attribute. The text inside an alt attribute is used for screen readers to improve accessibility and is displayed if the image fails to load.

Note: If the image is purely decorative, using an empty alt attribute is a best practice. Ideally the alt attribute should not contain special characters unless needed.

```html
<img src="https://www.imageurl.com/image.jpg" alt="Image description." />
```

You can use a (anchor) elements to link to content outside of your web page. a elements need a destination web address called an href attribute. They also need anchor text.

```html
<a href="https://www.freecodecamp.org" target="_blank">
  Link to freecodecamp.org
</a>
```

A target is an anchor tag attribute that specifies where to open the link. The value \_blank specifies to open the link in a new tab. The href is an anchor tag attribute that contains the URL address of the link. The text, link to www.freecodecamp.org, within the a element is called anchor text, and will display the link to click.

a (anchor) elements can also be used to create internal links to jump to different sections within a webpage. To create an internal link, you assign a link's href attribute to a hash symbol # plus the value of the id attribute for the element that you want to internally link to. You then need to add the same id attribute to the element you are linking to. An id is an attribute that uniquely describes an element.

```html
<a href="#contacts-header">Contacts</a>
...
<h2 id="contacts-header">Contacts</h2>
```

You can nest links within other text elements.

```html
<p>
  Here's a
  <a target="_blank" href="https://www.freecodecamp.org">
    link to www.freecodecamp.org
  </a>
  for you to follow.
</p>
```

Sometimes you want to add a elements to your website before you know where they will link. This is also handy when you're changing the behavior of a link using JavaScript. Replace the href attribute value with a #, also known as a hash symbol, to create a dead link.

```html
<a href="#" target="_blank">Dead link</a>
```

You can make elements into links by nesting them within an a element. For example an image element.

```html
<a href="#"><img src="image-url" alt="image-description" /></a>
```

HTML has a special element for creating unordered lists, or bullet point style lists. Unordered lists start with an opening <ul> element, followed by any number of <li> elements. Finally, unordered lists close with a </ul>.

```html
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```

HTML has another special element for creating ordered lists, or numbered lists. Ordered lists start with an opening <ol> element, followed by any number of <li> elements. Finally, ordered lists are closed with the </ol> tag.

```html
<ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
```

input elements are a convenient way to get input from your user. Note that input elements are self-closing.

```html
<input type="text" />
```

Placeholder text is what is displayed in your input element before your user has inputted anything.

```html
<input type="text" placeholder="this is placeholder text" />
```

You can build web forms that actually submit data to a server using nothing more than pure HTML. You can do this by specifying an action attribute on your form element.

```html
<form action="url-where-you-want-to-submit-form-data">
  <input />
</form>
```

A submit button inside your form will send the data from your form to the URL you specified with your form's action attribute.

```html
<button type="submit">this button submits the form</button>
```

You can require specific form fields so that your user will not be able to submit your form until he or she has filled them out. For example, if you wanted to make a text input field required, you can just add the attribute required within your input element.

```html
<input type="text" required />
```

You can use radio buttons for questions where you want the user to only give you one answer out of multiple options. Radio buttons are a type of input. Each of your radio buttons can be nested within its own label element. By wrapping an input element inside of a label element it will automatically associate the radio button input with the label element surrounding it.

All related radio buttons should have the same name attribute to create a radio button group. By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.

```html
<label><input type="radio" name="indoor-outdoor" />Indoor</label>
```

It is considered best practice to set a for attribute on the label element, with a value that matches the value of the id attribute of the input element. This allows assistive technologies to create a linked relationship between the label and the related input element.

```html
<input id="indoor" type="radio" name="indoor-outdoor" />
<label for="indoor">Indoor</label>
```

We can also nest the input element within the label tags.

```html
<label for="indoor">
  <input id="indoor" type="radio" name="indoor-outdoor" />Indoor
</label>
```

Forms commonly use checkboxes for questions that may have more than one answer. Checkboxes are a type of input. Each of your checkboxes can be nested within its own label element. By wrapping an input element inside of a label element it will automatically associate the checkbox input with the label element surrounding it.

All related checkbox inputs should have the same name attribute. It is considered best practice to explicitly define the relationship between a checkbox input and its corresponding label by setting the for attribute on the label element to match the id attribute of the associated input element.

```html
<label for="loving">
  <input id="loving" type="checkbox" name="personality" />Loving
</label>
```

When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type radio and checkbox report their values from the value attribute.

```html
<label for="indoor">
  <input id="indoor" value="indoor" type="radio" name="indoor-outdoor" />Indoor
</label>
<label for="outdoor">
  <input
    id="outdoor"
    value="outdoor"
    type="radio"
    name="indoor-outdoor"
  />Outdoor
</label>
```

When the user submits the form with the indoor option selected, the form data will include the line: indoor-outdoor=indoor. This is from the name and value attributes of the "indoor" input. If you omit the value attribute, the submitted form data uses the default value, which is on. In this scenario, if the user clicked the "indoor" option and submitted the form, the resulting form data would be indoor-outdoor=on, which is not useful. So the value attribute needs to be set to something to identify the option.

You can set a checkbox or radio button to be checked by default using the checked attribute.

```html
<input type="radio" name="test-name" checked />
```

The div element (division element) is a general purpose container for other elements. The div element is probably the most commonly used HTML element of all. Just like any other non-self-closing element, you can open a div element with <div> and close it on another line with </div>.

There are a few elements that give overall structure to your page, and should be included in every HTML document. At the top of your document, you need to tell the browser which version of HTML your page is using. HTML is an evolving language, and is updated regularly. Most major browsers support the latest specification, which is HTML5. However, older web pages may use previous versions of the language.

You tell the browser this information by adding the <!DOCTYPE ...> tag on the first line, where the ... part is the version of HTML. For HTML5, you use <!DOCTYPE html>. The ! and uppercase DOCTYPE is important, especially for older browsers. The html is not case sensitive.

Next, the rest of your HTML code needs to be wrapped in html tags. The opening <html> goes directly below the <!DOCTYPE html> line, and the closing </html> goes at the end of the page. Your HTML code would go in the space between the two html tags.

```html
<!DOCTYPE html>
<html></html>
```

You can add another level of organization in your HTML document within the html tags with the head and body elements. Any markup with information about your page would go into the head tag. Then any markup with the content of the page (what displays for a user) would go into the body tag. Metadata elements, such as link, meta, title, and style, typically go inside the head element.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta />
  </head>
  <body>
    <div></div>
  </body>
</html>
```

</details>

<details><summary>Basic CSS</summary>

CSS, or Cascading Style Sheets, tell the browser how to display the text and other content that you write in HTML. With CSS, you can control the color, font, size, spacing, and many other aspects of HTML elements.

With CSS, there are hundreds of CSS properties that you can use to change the way an element looks on your page. For example the property that is responsible for the color of an element's text is the color style property. Note that it is a good practice to end inline style declarations with a ;.

```css
<h2 style="color: blue;">CatPhotoApp</h2>
```

With code above, you were styling that individual h2 element with inline CSS, which stands for Cascading Style Sheets. That's one way to specify the style of an element, but there's a better way to apply CSS. At the top of your code, create a style block.

```css
<style></style>
```

Inside that style block, you can create a CSS selector for all h2 elements and add a style rule.

```css
<style>
  h2 {
    color: red;
  }
</style>
```

Note that it's important to have both opening and closing curly braces ({ and }) around each element's style rule(s). You also need to make sure that your element's style definition is between the opening and closing style tags. Finally, be sure to add a semicolon to the end of each of your element's style rules.

Classes are reusable styles that can be added to HTML elements. Class declaration:

```
<style>
  .blue-text {
    color: blue;
  }
</style>
```

</details>

```css

```
