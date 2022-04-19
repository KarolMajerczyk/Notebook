# Notebook

FreeCodeCamp Notes

## Responsive Web Design Certification

<details><summary>Basic HTML and HTML5</summary>

HTML is a markup language that uses a special syntax or notation to describe the structure of a webpage to the browser. HTML elements usually have opening and closing tags that surround and give meaning to content. For example, different elements can describe text as a heading, paragraph, or list item. HTML elements are the building blocks of any webpage.

Most HTML elements have an opening tag and a closing tag. The only difference between opening and closing tags is the forward slash after the opening bracket of a closing tag. For example this is a heading element with opening and closing tag:

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

---

<details><summary>Basic CSS</summary>

CSS, or Cascading Style Sheets, tell the browser how to display the text and other content that you write in HTML. With CSS, you can control the color, font, size, spacing, and many other aspects of HTML elements.

With CSS, there are hundreds of CSS properties that you can use to change the way an element looks on your page. For example the property that is responsible for the color of an element's text is the color style property. It is a good practice to end inline style declarations with a semicolon ";".

```css
<h2 style="color: blue;">CatPhotoApp</h2>
```

With code above, you were styling that individual h2 element with inline CSS, which stands for Cascading Style Sheets. That's one way to specify the style of an element, but there's a better way to apply CSS. At the top of your code, create a style block.

```css
<style></style>
```

Inside that style block, you can create a CSS selector for all h2 elements and add a style rule.

```css
h2 {
  color: red;
}
```

Note that it's important to have both opening and closing curly braces ({ and }) around each element's style rule(s). You also need to make sure that your element's style definition is between the opening and closing style tags. Finally, be sure to add a semicolon to the end of each of your element's style rules.

Classes are reusable styles that can be added to HTML elements. Classes allow you to use the same CSS styles on multiple HTML elements. Class declaration:

```css
.blue-text {
  color: blue;
}
```

Note that in your CSS style element, class names start with a period. In your HTML elements' class attribute, the class name does not include the period. You can apply a class attribute to an HTML element like this:

```html
<h2 class="blue-text">CatPhotoApp</h2>
```

Font size is controlled by the font-size CSS property.

```css
h1 {
  font-size: 30px;
}
```

You can set which font an element should use, by using the font-family property.

```css
h2 {
  font-family: sans-serif;
}
```

In addition to common fonts that are found on most operating systems, we can also specify non-standard, custom web fonts for use on our website. There are many sources for web fonts on the Internet. For example Google Fonts is a free library of web fonts that you can use in your CSS by referencing the font's URL. To import a Google Font, you can copy the font's URL from the Google Fonts library and then paste it in your HTML.

```html
<link
  href="https://fonts.googleapis.com/css?family=Lobster"
  rel="stylesheet"
  type="text/css"
/>
```

Now we can use it like this:

```css
h2 {
  font-family: Lobster, sans-serif;
}
```

The second font name is optional, and is a fallback font in case the other specified font is not available.

Family names are case-sensitive and need to be wrapped in quotes if there is a space in the name. For example, you need quotes to use the "Open Sans" font, but not to use the Lobster font. There are several default fonts that are available in all browsers. These generic font families include monospace, serif and sans-serif. When one font isn't available, you can tell the browser to "degrade" to another font. Generic font family names are not case-sensitive. Also, they do not need quotes because they are CSS keywords.

CSS has a property called width that controls an element's width.

```css
.larger-image {
  width: 500px;
}
```

CSS borders have properties like style, color and width.

```css
.thin-red-border {
  border-color: red;
  border-width: 5px;
  border-style: solid;
}
```

We can round out corners with a CSS property called border-radius. In addition to pixels, you can also specify the border-radius using a percentage. For example 50% will create a circle;

```css
.thin-red-border {
  border-radius: 10px;
}
```

You can set an element's background color with the background-color property.

```css
.green-background {
  background-color: green;
}
```

In addition to classes, each HTML element can also have an id attribute. There are several benefits to using id attributes: You can use an id to style a single element and you can use them to select and modify specific elements with JavaScript. id attributes should be unique. Browsers won't enforce this, but it is a widely agreed upon best practice. Don't give more than one element the same id attribute.

```css
<h2 id="cat-photo-app">
```

One cool thing about id attributes is that, like classes, you can style them using CSS. However, an id is not reusable and should only be applied to one element. An id also has a higher specificity (importance) than a class so if both are applied to the same element and have conflicting styles, the styles of the id will be applied. Note that inside your style element, you always reference classes by putting a . in front of their names. You always reference ids by putting a # in front of their names.

```css
#cat-photo-element {
  background-color: green;
}
```

All HTML elements are essentially little rectangles. Three important properties control the space that surrounds each HTML element: padding, border, and margin.

An element's padding controls the amount of space between the element's content and its border.
An element's margin controls the amount of space between an element's border and surrounding elements.

```css
.box {
  padding: 10px;
  margin: 20px;
}
```

If you set an element's margin to a negative value, the element will grow larger.

```css
.box {
  margin: -20px;
}
```

Sometimes you will want to customize an element so that it has different amounts of padding on each of its sides. CSS allows you to control the padding of all four individual sides of an element with the padding-top, padding-right, padding-bottom, and padding-left properties.

```css
.box {
  padding-top: 40px;
  padding-left: 40px;
  padding-bottom: 20px;
  padding-right: 20px;
}
```

Instead of specifying an element's padding-top, padding-right, padding-bottom, and padding-left properties individually, you can specify them all in one line. These four values work like a clock: top, right, bottom, left, and will produce the exact same result as using the side-specific padding instructions.

```css
.box {
  padding: 10px 20px 10px 20px;
}
```

Sometimes you will want to customize an element so that it has a different margin on each of its sides. CSS allows you to control the margin of all four individual sides of an element with the margin-top, margin-right, margin-bottom, and margin-left properties.

```css
.box {
  margin-top: 40px;
  margin-right: 20px;
  margin-bottom: 20px;
  margin-left: 40px;
}
```

Instead of specifying an element's margin-top, margin-right, margin-bottom, and margin-left properties individually, you can specify them all in one line. These four values work like a clock: top, right, bottom, left, and will produce the exact same result as using the side-specific margin instructions.

```css
.box {
  margin: 10px 20px 10px 20px;
}
```

You have been adding id or class attributes to elements that you wish to specifically style. These are known as ID and class selectors. There are other CSS Selectors you can use to select custom groups of elements to style.

The [attr=value] attribute selector matches and styles elements with a specific attribute value. For example, the below code changes the margins of all elements with the attribute type and a corresponding value of radio:

```css
[type="radio"] {
  margin: 20px 0px 20px 0px;
}
```

The last several challenges all set an element's margin or padding with pixels (px). Pixels are a type of length unit, which is what tells the browser how to size or space an item. In addition to px, CSS has a number of different length unit options that you can use.

The two main types of length units are absolute and relative. Absolute units tie to physical units of length. For example, in and mm refer to inches and millimeters, respectively. Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.

Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font. If you use it to set the font-size property itself, it's relative to the parent's font-size.

Note: There are several relative unit options that are tied to the size of the viewport. They are covered in the Responsive Web Design Principles section.

Every HTML page has a body element.

We can prove that the body element exists here by giving it a background-color of black.

We can do this by adding the following to our style element:

body {
background-color: black;
}

Now we've proven that every HTML page has a body element, and that its body element can also be styled with CSS.

Remember, you can style your body element just like any other HTML element, and all your other elements will inherit your body element's styles.

Sometimes your HTML elements will receive multiple styles that conflict with one another.

For example, your h1 element can't be both green and pink at the same time.

Let's see what happens when we create a class that makes text pink, then apply it to an element. Will our class override the body element's color: green; CSS property?

Our pink-text class overrode our body element's CSS declaration!

We just proved that our classes will override the body element's CSS. So the next logical question is, what can we do to override our pink-text class?

Note: It doesn't matter which order the classes are listed in the HTML element.

However, the order of the class declarations in the <style> section is what is important. The second declaration will always take precedence over the first. Because .blue-text is declared second, it overrides the attributes of .pink-text.

We just proved that browsers read CSS from top to bottom in order of their declaration. That means that, in the event of a conflict, the browser will use whichever CSS declaration came last. Notice that if we even had put blue-text before pink-text in our h1 element's classes, it would still look at the declaration order and not the order of their use!

But we're not done yet. There are other ways that you can override CSS. Do you remember id attributes?

Let's override your pink-text and blue-text classes, and make your h1 element orange, by giving the h1 element an id and then styling that id.

Note: It doesn't matter whether you declare this CSS above or below pink-text class, since the id attribute will always take precedence.

So we've proven that id declarations override class declarations, regardless of where they are declared in your style element CSS.

There are other ways that you can override CSS. Do you remember inline styles?

<h1 style="color: green;">

Yay! We just proved that inline styles will override all the CSS declarations in your style element.

But wait. There's one last way to override CSS. This is the most powerful method of all. But before we do it, let's talk about why you would ever want to override CSS.

In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important.

Let's go all the way back to our pink-text class declaration. Remember that our pink-text class was overridden by subsequent class declarations, id declarations, and inline styles.

color: red !important;

Did you know there are other ways to represent colors in CSS? One of these ways is called hexadecimal code, or hex code for short.

We usually use decimals, or base 10 numbers, which use the symbols 0 to 9 for each digit. Hexadecimals (or hex) are base 16 numbers. This means it uses sixteen distinct symbols. Like decimals, the symbols 0-9 represent the values zero to nine. Then A,B,C,D,E,F represent the values ten to fifteen. Altogether, 0 to F can represent a digit in hexadecimal, giving us 16 total possible values. You can find more information about hexadecimal numbers here.

In CSS, we can use 6 hexadecimal digits to represent colors, two each for the red (R), green (G), and blue (B) components. For example, #000000 is black and is also the lowest possible value. You can find more information about the RGB color system here.

body {
color: #000000;
}

To review, hex codes use 6 hexadecimal digits to represent colors, two each for red (R), green (G), and blue (B) components.

From these three pure colors (red, green, and blue), we can vary the amounts of each to create over 16 million other colors!

For example, orange is pure red, mixed with some green, and no blue. In hex code, this translates to being #FFA500.

The digit 0 is the lowest number in hex code, and represents a complete absence of color.

The digit F is the highest number in hex code, and represents the maximum possible brightness.

Many people feel overwhelmed by the possibilities of more than 16 million colors. And it's difficult to remember hex code. Fortunately, you can shorten it.

For example, red's hex code #FF0000 can be shortened to #F00. This shortened form gives one digit for red, one digit for green, and one digit for blue.

This reduces the total number of possible colors to around 4,000. But browsers will interpret #FF0000 and #F00 as exactly the same color.

Another way you can represent colors in CSS is by using RGB values.

The RGB value for black looks like this:

rgb(0, 0, 0)
The RGB value for white looks like this:

rgb(255, 255, 255)
Instead of using six hexadecimal digits like you do with hex code, with RGB you specify the brightness of each color with a number between 0 and 255.

If you do the math, the two digits for one color equal 16 times 16, which gives us 256 total values. So RGB, which starts counting from zero, has the exact same number of possible values as hex code.

Here's an example of how you'd change the body background to orange using its RGB code.

body {
background-color: rgb(255, 165, 0);
}

Just like with hex code, you can mix colors in RGB by using combinations of different values.

CSS Variables are a powerful way to change many CSS style properties at once by changing only one value.

Follow the instructions below to see how changing just three values can change the styling of many elements.

To create a CSS variable, you just need to give it a name with two hyphens in front of it and assign it a value like this:

--penguin-skin: gray;
This will create a variable named --penguin-skin and assign it the value of gray. Now you can use that variable elsewhere in your CSS to change the value of other properties to gray.

After you create your variable, you can assign its value to other CSS properties by referencing the name you gave it.

background: var(--penguin-skin);
This will change the background of whatever element you are targeting to gray because that is the value of the --penguin-skin variable. Note that styles will not be applied unless the variable names are an exact match.

When using your variable as a CSS property value, you can attach a fallback value that your browser will revert to if the given variable is invalid.

Note: This fallback is not used to increase browser compatibility, and it will not work on IE browsers. Rather, it is used so that the browser has a color to display if it cannot find your variable.

Here's how you do it:

background: var(--penguin-skin, black);
This will set background to black if your variable wasn't set. Note that this can be useful for debugging.

When working with CSS you will likely run into browser compatibility issues at some point. This is why it's important to provide browser fallbacks to avoid potential problems.

When your browser parses the CSS of a webpage, it ignores any properties that it doesn't recognize or support. For example, if you use a CSS variable to assign a background color on a site, Internet Explorer will ignore the background color because it does not support CSS variables. In that case, the browser will use whatever value it has for that property. If it can't find any other value set for that property, it will revert to the default value, which is typically not ideal.

This means that if you do want to provide a browser fallback, it's as easy as providing another more widely supported value immediately before your declaration. That way an older browser will have something to fall back on, while a newer browser will just interpret whatever declaration comes later in the cascade.

<style>
  :root {
    --red-color: red;
  }
  .red-box {
    background: red;
    background: var(--red-color);
    height: 200px;
    width:200px;
  }
</style>
<div class="red-box"></div>

When you create a variable, it is available for you to use inside the selector in which you create it. It also is available in any of that selector's descendants. This happens because CSS variables are inherited, just like ordinary properties.

To make use of inheritance, CSS variables are often defined in the :root element.

:root is a pseudo-class selector that matches the root element of the document, usually the html element. By creating your variables in :root, they will be available globally and can be accessed from any other selector in the style sheet.

Define a variable named --penguin-belly in the :root selector and give it the value of pink. You can then see that the variable is inherited and that all the child elements which use it get pink backgrounds.

When you create your variables in :root they will set the value of that variable for the whole page.

You can then overwrite these variables by setting them again within a specific selector.
Change the value of --penguin-belly to white in the penguin class.

CSS Variables can simplify the way you use media queries.

For instance, when your screen is smaller or larger than your media query break point, you can change the value of a variable, and it will apply its style wherever it is used.

:root {
--penguin-size: 300px;
--penguin-skin: gray;
--penguin-belly: white;
--penguin-beak: orange;
}

@media (max-width: 350px) {
:root {
/_ Only change code below this line _/
--penguin-size: 200px;
--penguin-skin: black;
/_ Only change code above this line _/
}
}

</details>

---

<details><summary>Applied Visual Design</summary>

Visual design is a combination of typography, color theory, graphics, animation, page layout, and more to help deliver your unique message.

In this course, you'll learn how to apply these different elements of visual design to your webpages.

This section of the curriculum focuses on Applied Visual Design. The first group of challenges build on the given card layout to show a number of core principles.

Text is often a large part of web content. CSS has several options for how to align it with the text-align property.

text-align: justify; spaces the text so that each line has equal width.

text-align: center; centers the text

text-align: right; right-aligns the text

And text-align: left; (the default) left-aligns the text.

You can specify the width of an element using the width property in CSS. Values can be given in relative length units (such as em), absolute length units (such as px), or as a percentage of its containing parent element. Here's an example that changes the width of an image to 220px:

img {
width: 220px;
}

You can specify the height of an element using the height property in CSS, similar to the width property. Here's an example that changes the height of an image to 20px:

img {
height: 20px;
}

To make text bold, you can use the strong tag. This is often used to draw attention to text and symbolize that it is important. With the strong tag, the browser applies the CSS of font-weight: bold; to the element.

To underline text, you can use the u tag. This is often used to signify that a section of text is important, or something to remember. With the u tag, the browser applies the CSS of text-decoration: underline; to the element.

Note: Try to avoid using the u tag when it could be confused for a link. Anchor tags also have a default underlined formatting.

To emphasize text, you can use the em tag. This displays text as italicized, as the browser applies the CSS of font-style: italic; to the element.

To strikethrough text, which is when a horizontal line cuts across the characters, you can use the s tag. It shows that a section of text is no longer valid. With the s tag, the browser applies the CSS of text-decoration: line-through; to the element.

You can use the hr tag to add a horizontal line across the width of its containing element. This can be used to define a change in topic or to visually separate groups of content.

Note: In HTML, hr is a self-closing tag, and therefore doesn't need a separate closing tag.

Instead of adjusting your overall background or the color of the text to make the foreground easily readable, you can add a background-color to the element holding the text you want to emphasize. This challenge uses rgba() instead of hex codes or normal rgb().

rgba stands for:
r = red
g = green
b = blue
a = alpha/level of opacity

The RGB values can range from 0 to 255. The alpha value can range from 1, which is fully opaque or a solid color, to 0, which is fully transparent or clear. rgba() is great to use in this case, as it allows you to adjust the opacity. This means you don't have to completely block out the background.

You'll use background-color: rgba(45, 45, 45, 0.1) for this challenge. It produces a dark gray color that is nearly transparent given the low opacity value of 0.1.

The font size of heading elements (h1 through h6) should generally be larger than the font size of paragraph tags. This makes it easier for the user to visually understand the layout and level of importance of everything on the page. You use the font-size property to adjust the size of the text in an element.

The box-shadow property applies one or more shadows to an element.

The box-shadow property takes the following values, in order:

offset-x (how far to push the shadow horizontally from the element)
offset-y (how far to push the shadow vertically from the element)
blur-radius
spread-radius
color
The blur-radius and spread-radius values are optional.

Multiple box-shadows can be created by using commas to separate properties of each box-shadow element.

Here's an example of the CSS to create multiple shadows with some blur, at mostly-transparent black colors:

box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);

The opacity property in CSS is used to adjust the opacity, or conversely, the transparency for an item.

A value of 1 is opaque, which isn't transparent at all.
A value of 0.5 is half see-through.
A value of 0 is completely transparent.
The value given will apply to the entire element, whether that's an image with some transparency, or the foreground and background colors for a block of text.

The text-transform property in CSS is used to change the appearance of text. It's a convenient way to make sure text on a webpage appears consistently, without having to change the text content of the actual HTML elements.

The following table shows how the different text-transformvalues change the example text "Transform me".

Value Result
lowercase "transform me"
uppercase "TRANSFORM ME"
capitalize "Transform Me"
initial Use the default value
inherit Use the text-transform value from the parent element
none Default: Use the original text

The font-size property is used to specify how large the text is in a given element. This rule can be used for multiple elements to create visual consistency of text on a page. In this challenge, you'll set the values for all h1 through h6 tags to balance the heading sizes.

In the style tags, set the font-size of the:

h1 tag to 68px.
h2 tag to 52px.
h3 tag to 40px.
h4 tag to 32px.
h5 tag to 21px.
h6 tag to 14px.

You set the font-size of each heading tag in the last challenge, here you'll adjust the font-weight.

The font-weight property sets how thick or thin characters are in a section of text.

Set the font-weight of the h1 tag to 800.
Set the font-weight of the h2 tag to 600.
Set the font-weight of the h3 tag to 500.
Set the font-weight of the h4 tag to 400.
Set the font-weight of the h5 tag to 300.
Set the font-weight of the h6 tag to 200.

The font-size property in CSS is not limited to headings, it can be applied to any element containing text.

CSS offers the line-height property to change the height of each line in a block of text. As the name suggests, it changes the amount of vertical space that each line of text gets.

This challenge will touch on the usage of pseudo-classes. A pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.

For example, the styling of an anchor tag can be changed for its hover state using the :hover pseudo-class selector. Here's the CSS to change the color of the anchor tag to red during its hover state:

a:hover {
color: red;
}
The code editor has a CSS rule to style all a tags black. Add a rule so that when the user hovers over the a tag, the color is blue.

CSS treats each HTML element as its own box, which is usually referred to as the CSS Box Model. Block-level items automatically start on a new line (think headings, paragraphs, and divs) while inline items sit within surrounding content (like images or spans). The default layout of elements in this way is called the normal flow of a document, but CSS offers the position property to override it.

When the position of an element is set to relative, it allows you to specify how CSS should move it relative to its current position in the normal flow of the page. It pairs with the CSS offset properties of left or right, and top or bottom. These say how many pixels, percentages, or ems to move the item away from where it is normally positioned. The following example moves the paragraph 10 pixels away from the bottom:

p {
position: relative;
bottom: 10px;
}
Changing an element's position to relative does not remove it from the normal flow - other elements around it still behave as if that item were in its default position.

Note: Positioning gives you a lot of flexibility and power over the visual layout of a page. It's good to remember that no matter the position of elements, the underlying HTML markup should be organized and make sense when read from top to bottom. This is how users with visual impairments (who rely on assistive devices like screen readers) access your content.

Change the position of the h2 to relative, and use a CSS offset to move it 15 pixels away from the top of where it sits in the normal flow. Notice there is no impact on the positions of the surrounding h1 and p elements.

Notice there is no impact on the positions of the surrounding h1 and p elements.
h2 {
position: relative;
top: 15px;

}

The CSS offsets of top or bottom, and left or right tell the browser how far to offset an item relative to where it would sit in the normal flow of the document. You're offsetting an element away from a given spot, which moves the element away from the referenced side (effectively, the opposite direction). As you saw in the last challenge, using the top offset moved the h2 downwards. Likewise, using a left offset moves an item to the right.

The next option for the CSS position property is absolute, which locks the element in place relative to its parent container. Unlike the relative position, this removes the element from the normal flow of the document, so surrounding items ignore it. The CSS offset properties (top or bottom and left or right) are used to adjust the position.

One nuance with absolute positioning is that it will be locked relative to its closest positioned ancestor. If you forget to add a position rule to the parent item, (this is typically done using position: relative;), the browser will keep looking up the chain and ultimately default to the body tag.

#searchbar {
position: absolute;
top: 50px;
right: 50px;

}

The next layout scheme that CSS offers is the fixed position, which is a type of absolute positioning that locks an element relative to the browser window. Similar to absolute positioning, it's used with the CSS offset properties and also removes the element from the normal flow of the document. Other items no longer "realize" where it is positioned, which may require some layout adjustments elsewhere.

One key difference between the fixed and absolute positions is that an element with a fixed position won't move when the user scrolls.

#navbar {
position: fixed;
top: 0;
left: 0;

    width: 100%;
    background-color: #767676;

}

The next positioning tool does not actually use position, but sets the float property of an element. Floating elements are removed from the normal flow of a document and pushed to either the left or right of their containing parent element. It's commonly used with the width property to specify how much horizontal space the floated element requires.

 <style>
    #left {
float: left;
      width: 50%;
    }
    #right {
float: right;
      width: 40%;
    }
    aside, section {
      padding: 2px;
      background-color: #ccc;
    }
  </style>

When elements are positioned to overlap (i.e. using position: absolute | relative | fixed | sticky), the element coming later in the HTML markup will, by default, appear on the top of the other elements. However, the z-index property can specify the order of how elements are stacked on top of one another. It must be an integer (i.e. a whole number and not a decimal), and higher values for the z-index property of an element move it higher in the stack than those with lower values.

.first {
background-color: red;
position: absolute;
z-index: 2;
}

Another positioning technique is to center a block element horizontally. One way to do this is to set its margin to a value of auto.

This method works for images, too. Images are inline elements by default, but can be changed to block elements when you set the display property to block.

div {
background-color: blue;
height: 100px;
width: 100px;
margin: auto;
}

Color theory and its impact on design is a deep topic and only the basics are covered in the following challenges. On a website, color can draw attention to content, evoke emotions, or create visual harmony. Using different combinations of colors can really change the look of a website, and a lot of thought can go into picking a color palette that works with your content.

The color wheel is a useful tool to visualize how colors relate to each other - it's a circle where similar hues are neighbors and different hues are farther apart. When two colors are opposite each other on the wheel, they are called complementary colors. They have the characteristic that if they are combined, they "cancel" each other out and create a gray color. However, when placed side-by-side, these colors appear more vibrant and produce a strong visual contrast.

Some examples of complementary colors with their hex codes are:

red (#FF0000) and cyan (#00FFFF)
green (#00FF00) and magenta (#FF00FF)
blue (#0000FF) and yellow (#FFFF00)

This is different than the outdated RYB color model that many of us were taught in school, which has different primary and complementary colors. Modern color theory uses the additive RGB model (like on a computer screen) and the subtractive CMY(K) model (like in printing). Read here for more information on this complex subject.

There are many color picking tools available online that have an option to find the complement of a color.

Note: Using color can be a powerful way to add visual interest to a page. However, color alone should not be used as the only way to convey important information because users with visual impairments may not understand that content. This issue will be covered in more detail in the Applied Accessibility challenges.

Computer monitors and device screens create different colors by combining amounts of red, green, and blue light. This is known as the RGB additive color model in modern color theory. Red (R), green (G), and blue (B) are called primary colors. Mixing two primary colors creates the secondary colors cyan (G + B), magenta (R + B) and yellow (R + G). You saw these colors in the Complementary Colors challenge. These secondary colors happen to be the complement to the primary color not used in their creation, and are opposite to that primary color on the color wheel. For example, magenta is made with red and blue, and is the complement to green.

Tertiary colors are the result of combining a primary color with one of its secondary color neighbors. For example, within the RGB color model, red (primary) and yellow (secondary) make orange (tertiary). This adds six more colors to a simple color wheel for a total of twelve.

There are various methods of selecting different colors that result in a harmonious combination in design. One example that can use tertiary colors is called the split-complementary color scheme. This scheme starts with a base color, then pairs it with the two colors that are adjacent to its complement. The three colors provide strong visual contrast in a design, but are more subtle than using two complementary colors.

Here are three colors created using the split-complement scheme:

Color Hex Code
orange #FF7F00
cyan #00FFFF
raspberry #FF007F

The Complementary Colors challenge showed that opposite colors on the color wheel can make each other appear more vibrant when placed side-by-side. However, the strong visual contrast can be jarring if it's overused on a website, and can sometimes make text harder to read if it's placed on a complementary-colored background. In practice, one of the colors is usually dominant and the complement is used to bring visual attention to certain content on the page.

Colors have several characteristics including hue, saturation, and lightness. CSS3 introduced the hsl() function as an alternative way to pick a color by directly stating these characteristics.

Hue is what people generally think of as 'color'. If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line. In hsl(), hue uses a color wheel concept instead of the spectrum, where the angle of the color on the circle is given as a value between 0 and 360.

Saturation is the amount of gray in a color. A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray. This is given as a percentage with 100% being fully saturated.

Lightness is the amount of white or black in a color. A percentage is given ranging from 0% (black) to 100% (white), where 50% is the normal color.

Here are a few examples of using hsl() with fully-saturated, normal lightness colors:

Color HSL
red hsl(0, 100%, 50%)
yellow hsl(60, 100%, 50%)
green hsl(120, 100%, 50%)
cyan hsl(180, 100%, 50%)
blue hsl(240, 100%, 50%)
magenta hsl(300, 100%, 50%)

The hsl() option in CSS also makes it easy to adjust the tone of a color. Mixing white with a pure hue creates a tint of that color, and adding black will make a shade. Alternatively, a tone is produced by adding gray or by both tinting and shading. Recall that the 's' and 'l' of hsl() stand for saturation and lightness, respectively. The saturation percent changes the amount of gray and the lightness percent determines how much white or black is in the color. This is useful when you have a base hue you like, but need different variations of it.

Applying a color on HTML elements is not limited to one flat hue. CSS provides the ability to use color transitions, otherwise known as gradients, on elements. This is accessed through the background property's linear-gradient() function. Here is the general syntax:

background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);

The first argument specifies the direction from which color transition starts - it can be stated as a degree, where 90deg makes a horizontal gradient (from left to right) and 45deg makes a diagonal gradient (from bottom left to top right). The following arguments specify the order of colors used in the gradient.

Example:

background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255))

The repeating-linear-gradient() function is very similar to linear-gradient() with the major difference that it repeats the specified gradient pattern. repeating-linear-gradient() accepts a variety of values, but for simplicity, you'll work with an angle value and color stop values in this challenge.

The angle value is the direction of the gradient. Color stops are like width values that mark where a transition takes place, and are given with a percentage or a number of pixels.

In the example demonstrated in the code editor, the gradient starts with the color yellow at 0 pixels which blends into the second color blue at 40 pixels away from the start. Since the next color stop is also at 40 pixels, the gradient immediately changes to the third color green, which itself blends into the fourth color value red as that is 80 pixels away from the beginning of the gradient.

For this example, it helps to think about the color stops as pairs where every two colors blend together.

0px [yellow -- blend -- blue] 40px [green -- blend -- red] 80px

If every two color stop values are the same color, the blending isn't noticeable because it's between the same color, followed by a hard transition to the next color, so you end up with stripes.

background: repeating-linear-gradient(
45deg,
yellow 0px,
yellow 40px,
black 40px,
black 80px
);

One way to add texture and interest to a background and have it stand out more is to add a subtle pattern. The key is balance, as you don't want the background to stand out too much, and take away from the foreground. The background property supports the url() function in order to link to an image of the chosen texture or pattern. The link address is wrapped in quotes inside the parentheses.

body {
background: url( https://cdn-media-1.freecodecamp.org/imgr/MJAkxbh.png);
}

To change the scale of an element, CSS has the transform property, along with its scale() function. The following code example doubles the size of all the paragraph elements on the page:

p {
transform: scale(2);
}

The transform property has a variety of functions that let you scale, move, rotate, skew, etc., your elements. When used with pseudo-classes such as :hover that specify a certain state of an element, the transform property can easily add interactivity to your elements.

Here's an example to scale the paragraph elements to 2.1 times their original size when a user hovers over them:

p:hover {
transform: scale(2.1);
}
Note: Applying a transform to a div element will also affect any child elements contained in the div.

The next function of the transform property is skewX(), which skews the selected element along its X (horizontal) axis by a given degree.

The following code skews the paragraph element by -32 degrees along the X-axis.

p {
transform: skewX(-32deg);
}

Given that the skewX() function skews the selected element along the X-axis by a given degree, it is no surprise that the skewY() property skews an element along the Y (vertical) axis.

#top {
background-color: red;
transform: skewY(-10deg);
}

By manipulating different selectors and properties, you can make interesting shapes. One of the easier ones to try is a crescent moon shape. For this challenge you need to work with the box-shadow property that sets the shadow of an element, along with the border-radius property that controls the roundness of the element's corners.

You will create a round, transparent object with a crisp shadow that is slightly offset to the side - the shadow is actually going to be the moon shape you see.

In order to create a round object, the border-radius property should be set to a value of 50%.

You may recall from an earlier challenge that the box-shadow property takes values for offset-x, offset-y, blur-radius, spread-radius and a color value in that order. The blur-radius and spread-radius values are optional.

.center {
position: absolute;
margin: auto;
top: 0;
right: 0;
bottom: 0;
left: 0;
width: 100px;
height: 100px;
background-color: transparent;
border-radius: 50%;
box-shadow: 25px 10px 0 0 blue;
}

One of the most popular shapes in the world is the heart shape, and in this challenge you'll create one using pure CSS. But first, you need to understand the ::before and ::after pseudo-elements. ::before creates a pseudo-element that is the first child of the selected element; ::after creates a pseudo-element that is the last child of the selected element. In the following example, a ::before pseudo-element is used to add a rectangle to an element with the class heart:

.heart::before {
content: "";
background-color: yellow;
border-radius: 25%;
position: absolute;
height: 50px;
width: 70px;
top: -50px;
left: 5px;
}

For the ::before and ::after pseudo-elements to function properly, they must have a defined content property. This property is usually used to add things like a photo or text to the selected element. When the ::before and ::after pseudo-elements are used to make shapes, the content property is still required, but it's set to an empty string. In the above example, the element with the class of heart has a ::before pseudo-element that produces a yellow rectangle with height and width of 50px and 70px, respectively. This rectangle has round corners due to its 25% border-radius and is positioned absolutely at 5px from the left and 50px above the top of the element.

<style>
  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
  }
  .heart::after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart::before {
    content: "";
    background-color: pink;
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }
</style>
<div class="heart"></div>

To animate an element, you need to know about the animation properties and the @keyframes rule. The animation properties control how the animation should behave and the @keyframes rule controls what happens during that animation. There are eight animation properties in total. This challenge will keep it simple and cover the two most important ones first:

animation-name sets the name of the animation, which is later used by @keyframes to tell CSS which rules go with which animations.

animation-duration sets the length of time for the animation.

@keyframes is how to specify exactly what happens within the animation over the duration. This is done by giving CSS properties for specific "frames" during the animation, with percentages ranging from 0% to 100%. If you compare this to a movie, the CSS properties for 0% is how the element displays in the opening scene. The CSS properties for 100% is how the element appears at the end, right before the credits roll. Then CSS applies the magic to transition the element over the given duration to act out the scene. Here's an example to illustrate the usage of @keyframes and the animation properties:

#anim {
animation-name: colorful;
animation-duration: 3s;
}

@keyframes colorful {
0% {
background-color: blue;
}
100% {
background-color: yellow;
}
}

For the element with the anim id, the code snippet above sets the animation-name to colorful and sets the animation-duration to 3 seconds. Then the @keyframes rule links to the animation properties with the name colorful. It sets the color to blue at the beginning of the animation (0%) which will transition to yellow by the end of the animation (100%). You aren't limited to only beginning-end transitions, you can set properties for the element for any percentage between 0% and 100%.

You can use CSS @keyframes to change the color of a button in its hover state.

Here's an example of changing the width of an image on hover:

<style>
  img {
    width: 30px;
  }
  img:hover {
    animation-name: width;
    animation-duration: 500ms;
  }

  @keyframes width {
    100% {
      width: 40px;
    }
  }
</style>

<img src="https://cdn.freecodecamp.org/curriculum/applied-visual-design/google-logo.png" alt="Google's Logo" />

Note that ms stands for milliseconds, where 1000ms is equal to 1s.

Use CSS @keyframes to change the background-color of the button element so it becomes #4791d0 when a user hovers over it. The @keyframes rule should only have an entry for 100%.

Note that ms stands for milliseconds, where 1000ms is equal to 1s.

That's great, but it doesn't work right yet. Notice how the animation resets after 500ms has passed, causing the button to revert back to the original color. You want the button to stay highlighted.

This can be done by setting the animation-fill-mode property to forwards. The animation-fill-mode specifies the style applied to an element when the animation has finished. You can set it like so:

animation-fill-mode: forwards;

When elements have a specified position, such as fixed or relative, the CSS offset properties right, left, top, and bottom can be used in animation rules to create movement.

As shown in the example below, you can push the item downwards then upwards by setting the top property of the 50% keyframe to 50px, but having it set to 0px for the first (0%) and the last (100%) keyframe.

@keyframes rainbow {
0% {
background-color: blue;
top: 0px;
}
50% {
background-color: green;
top: 50px;
}
100% {
background-color: yellow;
top: 0px;
}
}

For this challenge, you'll change the opacity of an animated element so it gradually fades as it reaches the right side of the screen.

In the displayed animation, the round element with the gradient background moves to the right by the 50% mark of the animation per the @keyframes rule.

@keyframes fade {
50% {
left: 60%;
opacity: 0.1;

    }

}

The previous challenges covered how to use some of the animation properties and the @keyframes rule. Another animation property is the animation-iteration-count, which allows you to control how many times you would like to loop through the animation. Here's an example:

animation-iteration-count: 3;

In this case the animation will stop after running 3 times, but it's possible to make the animation run continuously by setting that value to infinite.

Here's one more continuous animation example with the animation-iteration-count property that uses the heart you designed in a previous challenge.

The one-second long heartbeat animation consists of two animated pieces. The heart elements (including the :before and :after pieces) are animated to change size using the transform property, and the background div is animated to change its color using the background property.

There are a variety of ways to alter the animation rates of similarly animated elements. So far, this has been achieved by applying an animation-iteration-count property and setting @keyframes rules.

To illustrate, the animation on the right consists of two stars that each decrease in size and opacity at the 20% mark in the @keyframes rule, which creates the twinkle animation. You can change the @keyframes rule for one of the elements so the stars twinkle at different rates.

In the previous challenge, you changed the animation rates for two similarly animated elements by altering their @keyframes rules. You can achieve the same goal by manipulating the animation-duration of multiple elements.

In the animation running in the code editor, there are three stars in the sky that twinkle at the same rate on a continuous loop. To make them twinkle at different rates, you can set the animation-duration property to different values for each element.

In CSS animations, the animation-timing-function property controls how quickly an animated element changes over the duration of the animation. If the animation is a car moving from point A to point B in a given time (your animation-duration), the animation-timing-function says how the car accelerates and decelerates over the course of the drive.

There are a number of predefined keywords available for popular options. For example, the default value is ease, which starts slow, speeds up in the middle, and then slows down again in the end. Other options include ease-out, which is quick in the beginning then slows down, ease-in, which is slow in the beginning, then speeds up at the end, or linear, which applies a constant animation speed throughout.

The last challenge introduced the animation-timing-function property and a few keywords that change the speed of an animation over its duration. CSS offers an option other than keywords that provides even finer control over how the animation plays out, through the use of Bezier curves.

In CSS animations, Bezier curves are used with the cubic-bezier function. The shape of the curve represents how the animation plays out. The curve lives on a 1 by 1 coordinate system. The X-axis of this coordinate system is the duration of the animation (think of it as a time scale), and the Y-axis is the change in the animation.

The cubic-bezier function consists of four main points that sit on this 1 by 1 grid: p0, p1, p2, and p3. p0 and p3 are set for you - they are the beginning and end points which are always located respectively at the origin (0, 0) and (1, 1). You set the x and y values for the other two points, and where you place them in the grid dictates the shape of the curve for the animation to follow. This is done in CSS by declaring the x and y values of the p1 and p2 "anchor" points in the form: (x1, y1, x2, y2). Pulling it all together, here's an example of a Bezier curve in CSS code:

animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);
In the example above, the x and y values are equivalent for each point (x1 = 0.25 = y1 and x2 = 0.75 = y2), which if you remember from geometry class, results in a line that extends from the origin to point (1, 1). This animation is a linear change of an element during the length of an animation, and is the same as using the linear keyword. In other words, it changes at a constant speed.

A previous challenge discussed the ease-out keyword that describes an animation change that speeds up first and then slows down at the end of the animation. On the right, the difference between the ease-out keyword (for the blue element) and linear keyword (for the red element) is demonstrated. Similar animation progressions to the ease-out keyword can be achieved by using a custom cubic Bezier curve function.

In general, changing the p1 and p2 anchor points drives the creation of different Bezier curves, which controls how the animation progresses through time. Here's an example of a Bezier curve using values to mimic the ease-out style:

animation-timing-function: cubic-bezier(0, 0, 0.58, 1);
Remember that all cubic-bezier functions start with p0 at (0, 0) and end with p3 at (1, 1). In this example, the curve moves faster through the Y-axis (starts at 0, goes to p1 y value of 0, then goes to p2 y value of 1) than it moves through the X-axis (0 to start, then 0 for p1, up to 0.58 for p2). As a result, the change in the animated element progresses faster than the time of the animation for that segment. Towards the end of the curve, the relationship between the change in x and y values reverses - the y value moves from 1 to 1 (no change), and the x values move from 0.58 to 1, making the animation changes progress slower compared to the animation duration.

This challenge animates an element to replicate the movement of a ball being juggled. Prior challenges covered the linear and ease-out cubic Bezier curves, however neither depicts the juggling movement accurately. You need to customize a Bezier curve for this.

The animation-timing-function automatically loops at every keyframe when the animation-iteration-count is set to infinite. Since there is a keyframe rule set in the middle of the animation duration (at 50%), it results in two identical animation progressions at the upward and downward movement of the ball.

The following cubic Bezier curve simulates a juggling movement:

cubic-bezier(0.3, 0.4, 0.5, 1.6);
Notice that the value of y2 is larger than 1. Although the cubic Bezier curve is mapped on a 1 by 1 coordinate system, and it can only accept x values from 0 to 1, the y value can be set to numbers larger than one. This results in a bouncing movement that is ideal for simulating the juggling ball.

  </details>

---

<details><summary>Applied Accessibility</summary>

The alt text in an alt attribute describes the image's content and provides a text-alternative for it. An alt attribute helps in cases where the image fails to load or can't be seen by a user. Search engines also use it to understand what an image contains to include it in search results. People with visual impairments rely on screen readers to convert web content to an audio interface. They won't get information if it's only presented visually. For images, screen readers can access the alt attribute and read its contents to deliver key information. Good alt text provides the reader a brief description of the image. You should always include an alt attribute on your image. Per HTML5 specification, this is now considered mandatory.

```html
<img src="importantLogo.jpeg" alt="Company logo" />
```

Sometimes images are grouped with a caption already describing them, or are used for decoration only. In these cases, alt text may seem redundant or unnecessary. When an image is already explained with text content or does not add meaning to a page, the img still needs an alt attribute, but it can be set to an empty string. Background images usually fall under the 'decorative' label as well. However, they are typically applied with CSS rules, and therefore not part of the markup screen readers process. For images with a caption, you may still want to include alt text since it helps search engines catalog the image's content.

```html
<img src="visualDecoration.jpeg" alt="" />
```

Headings (h1 through h6 elements) are tags that help provide structure and labeling to your content. Screen readers can be set to read only the headings on a page so the user gets a summary. This means it is important for the heading tags in your markup to have semantic meaning and relate to each other, not be picked merely for their size values. Semantic meaning means that the tag you use around content indicates the type of information it contains. The heading tags in a webpage need to go in order and indicate the hierarchical relationships of your content. Headings with equal (or higher) rank start new implied sections, headings with lower rank start subsections of the previous one. Each page should always have only one h1 element, which is the main subject of your content. This and the other headings are used in part by search engines to understand the topic of the page.

HTML5 introduced several new elements that give developers more options while also incorporating accessibility features. These tags include main, header, footer, nav, article, and section, among others. By default, a browser renders these elements similar to the humble div. However, using them where appropriate gives additional meaning to your markup. The tag name alone can indicate the type of information it contains, which adds semantic meaning to that content. Assistive technologies can access this information to provide better page summary or navigation options to their users.

The main element is used to wrap the main content, and there should be only one per page. It's meant to surround the information related to your page's central topic. It's not meant to include items that repeat across pages, like navigation links or banners. The main tag also has an embedded landmark feature that assistive technology can use to navigate to the main content quickly ("Jump to Main Content"). Using the main tag automatically gives assistive devices that functionality.

The article tag is a sectioning element and is used to wrap independent, self-contained content. The tag works well with blog entries, forum posts, or news articles. Determining whether content can stand alone is usually a judgment call, but you can use a couple of simple tests. Ask yourself if you removed all surrounding context, would that content still make sense? Similarly, for text, would the content hold up if it were in an RSS feed?

Remember that folks using assistive technologies rely on organized, semantically meaningful markup to better understand your work.

The section element has a slightly different semantic meaning than article. An article is for standalone content, and a section is for grouping thematically related content. They can be used within each other, as needed. For example, if a book is the article, then each chapter is a section. When there's no relationship between groups of content, then use a div.

- <div> - groups content
- <section> - groups related content
- <article> - groups independent, self-contained content

The header tag is used to wrap introductory information or navigation links for its parent tag and works well around content that's repeated at the top on multiple pages. The header element also allows assistive technologies to quickly navigate to that content. The header is meant for use in the body tag of your HTML document. It is different than the head element, which contains the page's title, meta information, etc.

```html
<header>
  <h1>Training with Camper Cat</h1>
</header>
```

The nav element is another HTML5 item with the embedded landmark feature for easy screen reader navigation. This tag is meant to wrap around the main navigation links in your page. If there are repeated site links at the bottom of the page, it isn't necessary to markup those with a nav tag as well. Using a footer is sufficient.

```html
<nav>
  <ul>
    <li><a href="#stealth">Stealth &amp; Agility</a></li>
    <li><a href="#combat">Combat</a></li>
    <li><a href="#weapons">Weapons</a></li>
  </ul>
</nav>
```

The footer element has also a built-in landmark feature that allows assistive devices to quickly navigate to it. It's primarily used to contain copyright information or links to related documents that usually sit at the bottom of a page.

HTML5's audio element gives semantic meaning when it wraps sound or audio stream content in your markup. Audio content also needs a text alternative to be accessible to people who are deaf or hard of hearing. This can be done with nearby text on the page or a link to a transcript. The audio tag supports the controls attribute. This shows the browser default play, pause, and other controls, and supports keyboard functionality. This is a boolean attribute, meaning it doesn't need a value, its presence on the tag turns the setting on.

```html
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```

Multimedia content usually has both visual and auditory components. It needs synchronized captions and a transcript so users with visual and/or auditory impairments can access it. A web developer is not responsible for creating the captions or transcript, but needs to know to include them.

HTML5 introduced the figure element and the related figcaption. Used together, these items wrap a visual representation along with its caption. Wrapping these elements together gives a two-fold accessibility boost by semantically grouping related content and providing a text alternative explaining the figure. For data visualizations like charts, the caption can be used to briefly note the trends or conclusions for users with visual impairments.

```html
<figure>
  <img
    src="roundhouseDestruction.jpeg"
    alt="Photo of Camper Cat executing a roundhouse kick"
  />
  <br />
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>
```

Improving accessibility with semantic HTML markup applies to using both appropriate tag names and attributes. The label tag wraps the text for a specific form control item, usually the name or label for a choice. This ties meaning to the item and makes the form more readable. The for attribute on a label tag explicitly associates that label with the form control and is used by screen readers.

Before we wrapped the radio button input element inside a label element along with the label text in order to make the text clickable. Another way to achieve this is by using the for attribute. The value of the for attribute must be the same as the value of the id attribute of the form control.

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" />
</form>
```

WIth radio buttons each choice is given a label with a for attribute tying to the id of the corresponding item. Since radio buttons often come in a group where the user must choose one, there's a way to semantically show the choices are part of a set. The fieldset tag surrounds the entire grouping of radio buttons to achieve this. It often uses a legend tag to provide a description for the grouping, which screen readers read for each choice in the fieldset element. The fieldset wrapper and legend tag are not necessary when the choices are self-explanatory, like a gender selection. Using a label with the for attribute for each radio button is sufficient.

```html
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one" />
    <label for="one">Choice One</label><br />
    <input id="two" type="radio" name="items" value="two" />
    <label for="two">Choice Two</label><br />
    <input id="three" type="radio" name="items" value="three" />
    <label for="three">Choice Three</label>
  </fieldset>
</form>
```

Forms often include the input field, which can be used to create several different form controls. The type attribute on this element indicates what kind of input element will be created. HTML5 introduced an option to specify a date field. Depending on browser support, a date picker shows up in the input field when it's in focus, which makes filling in a form easier for all users. For older browsers, the type will default to text, so it helps to show users the expected date format in the label or placeholder text just in case.

```html
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1" />
```

HTML5 also introduced the time element along with a datetime attribute to standardize times. The time element is an inline element that can wrap a date or time on a page. A datetime attribute holds a valid format of that date. This is the value accessed by assistive devices. It helps avoid confusion by stating a standardized version of a time, even if it's informally or colloquially written in the text.

```html
<p>
  Master Camper Cat officiated the cage match between Goro and Scorpion
  <time datetime="2013-02-13">last Wednesday</time>, which ended in a draw.
</p>
```

For accessibility it is important to use a logical document outline and semantically meaningful tags around your content before introducing the visual design aspect. However, CSS can also improve accessibility on your page when you want to visually hide content meant only for screen readers. This happens when information is in a visual format (like a chart), but screen reader users need an alternative presentation (like a table) to access the data. CSS is used to position the screen reader-only elements off the visual area of the browser window.

```css
.sr-only {
  position: absolute;
  left: -10000px;
  width: 1px;
  height: 1px;
  top: auto;
  overflow: hidden;
}
```

The following CSS approaches will NOT do the same thing:

- display: none; or visibility: hidden; hides content for everyone, including screen reader users
- zero values for pixel sizes, such as width: 0px; height: 0px; removes that element from the flow of your document, meaning screen readers will ignore it

Low contrast between the foreground and background colors can make text difficult to read. Sufficient contrast improves your content's readability. The Web Content Accessibility Guidelines (WCAG) recommend at least a 4.5 to 1 contrast ratio for normal text as well as gray-scale combinations. The ratio is calculated by comparing the relative luminance values of two colors. This ranges from 1:1 for the same color, or no contrast, to 21:1 for white against black, the most substantial contrast. There are many contrast checking tools available online that calculate this ratio for you.

Color is a large part of visual design, but its use introduces two accessibility issues. First, color alone should not be used as the only way to convey important information because screen reader users won't see it. Second, foreground and background colors need sufficient contrast so colorblind users can distinguish them.

Colorblind users have trouble distinguishing some colors from others - usually in hue but sometimes lightness as well. The contrast ratio is calculated using the relative luminance (or lightness) values of the foreground and background colors. In practice, the 4.5:1 contrast ratio can be reached by shading (adding black to) the darker color and tinting (adding white to) the lighter color. Darker shades on the color wheel are considered to be shades of blues, violets, magentas, and reds, whereas lighter tinted colors are oranges, yellows, greens, and blue-greens.

There are various forms of colorblindness. These can range from a reduced sensitivity to a certain wavelength of light to the inability to see color at all. The most common form is a reduced sensitivity to detect greens. For example, if two similar green colors are the foreground and background color of your content, a colorblind user may not be able to distinguish them. Close colors can be thought of as neighbors on the color wheel, and those combinations should be avoided when conveying important information. Some online color picking tools include visual simulations of how colors appear for different types of colorblindness. These are great resources in addition to online contrast checking calculators.

Screen reader users have various options for what type of content their device reads. These options include skipping to (or over) landmark elements, jumping to the main content, or getting a page summary from the headings. Another option is to only hear the links available on a page. Screen readers do this by reading the link text, or what's between the anchor (a) tags. Having a list of "click here" or "read more" links isn't helpful. Instead, use brief but descriptive text within the a tags to provide more meaning for these users.

HTML offers the accesskey attribute to specify a shortcut key to activate or bring focus to an element. Adding an accesskey attribute can make navigation more efficient for keyboard-only users. HTML5 allows this attribute to be used on any element, but it's particularly useful when it's used with interactive ones. This includes links, buttons, and form controls.

```html
<button accesskey="b">Important Button</button>
```

The HTML tabindex attribute has three distinct functions relating to an element's keyboard focus. When it's on a tag, it indicates that the element can be focused on. The value (an integer that's positive, negative, or zero) determines the behavior. Certain elements, such as links and form controls, automatically receive keyboard focus when a user tabs through a page. It's in the same order as the elements come in the HTML source markup. This same functionality can be given to other elements, such as div, span, and p, by placing a tabindex="0" attribute on them. A negative tabindex value (typically -1) indicates that an element is focusable, but is not reachable by the keyboard. This method is generally used to bring focus to content programmatically (like when a div used for a pop-up window is activated). Using tabindex also enables the CSS pseudo-class :focus to work on the p tag.

```html
<div tabindex="0">I need keyboard focus!</div>
```

The tabindex attribute also specifies the exact tab order of elements. This is achieved when the attribute's value is set to a positive number of 1 or higher. Setting a tabindex="1" will bring keyboard focus to that element first. Then it cycles through the sequence of specified tabindex values (2, 3, etc.), before moving to default and tabindex="0" items. When the tab order is set this way, it overrides the default order (which uses the HTML source). This may confuse users who are expecting to start navigation from the top of the page. This technique may be necessary but be careful. Some browsers may place you in the middle of your tab order when an element is clicked. An element has been added to the page that ensures you will always start at the beginning of your tab order.

```html
<div tabindex="1">I get keyboard focus, and I get it first!</div>
<div tabindex="2">I get keyboard focus, and I get it second!</div>
```

</details>

---

<details><summary>Responsive Web Design Principles</summary>

Media Queries are a new technique introduced in CSS3 that change the presentation of content based on different viewport sizes. The viewport is a user's visible area of a web page, and is different depending on the device used to access the site. Media Queries consist of a media type, and if that media type matches the type of device the document is displayed on, the styles are applied. You can have as many selectors and styles inside your media query as you want. The CSS inside the media query is applied only if the media type matches that of the device being used.

An example, when the device's width is less than or equal to 100px:

```css
@media (max-width: 100px) { /_ CSS Rules _/ }
```

An example, when the device's height is more than or equal to 350px:

```css
@media (min-height: 350px) { /_ CSS Rules _/ }
```

Making images responsive with CSS is very simple. The max-width of 100% will make sure the image is never wider than the container it is in, and the height of auto will make the image keep its original aspect ratio.

```css
img {
  max-width: 100%;
  height: auto;
}
```

With the increase of internet connected devices, their sizes and specifications vary, and the displays they use could be different externally and internally. Pixel density is an aspect that could be different on one device from others and this density is known as Pixel Per Inch(PPI) or Dots Per Inch(DPI). The most famous such display is the one known as a "Retina Display" on the latest Apple MacBook Pro notebooks, and recently iMac computers. Due to the difference in pixel density between a "Retina" and "Non-Retina" displays, some images that have not been made with a High-Resolution Display in mind could look "pixelated" when rendered on a High-Resolution display. The simplest way to make your images properly appear on High-Resolution Displays, such as the MacBook Pros "retina display" is to define their width and height values as only half of what the original file is.

```css
<style>
  img { height: 250px; width: 250px; }
</style>
```

Instead of using em or px to size text, you can use viewport units for responsive typography. Viewport units, like percentages, are relative units, but they are based off different items. Viewport units are relative to the viewport dimensions (width or height) of a device, and percentages are relative to the size of the parent container element.

The four different viewport units are:

- vw (viewport width): 10vw would be 10% of the viewport's width.
- vh (viewport height): 3vh would be 3% of the viewport's height.
- vmin (viewport minimum): 70vmin would be 70% of the viewport's smaller dimension (height or width).
- vmax (viewport maximum): 100vmax would be 100% of the viewport's bigger dimension (height or width).

```css
body {
  width: 30vw;
}
```

</details>

<details><summary>CSS Flexbox</summary>

Placing the CSS property display: flex; on an element allows you to use other flex properties to build a responsive page.

Adding display: flex to an element turns it into a flex container. This makes it possible to align any children of that element into rows or columns. You do this by adding the flex-direction property to the parent item and setting it to row or column. Creating a row will align the children horizontally, and creating a column will align the children vertically. The default value for the flex-direction property is row. Other options for flex-direction are row-reverse and column-reverse.

Sometimes the flex items within a flex container do not fill all the space in the container.

Here is a image illustrating the concepts for a 'row' flex container.
https://www.w3.org/TR/css-flexbox-1/images/flex-direction-terms.svg

Setting a flex container as a row places the flex items side-by-side from left-to-right. A flex container set as a column places the flex items in a vertical stack from top-to-bottom. For each, the direction the flex items are arranged is called the main axis. For a row, this is a horizontal line that cuts through each item. And for a column, the main axis is a vertical line through the items.

There are several options for how to space the flex items along the line that is the main axis. One of the most commonly used is justify-content: center;, which aligns all the flex items to the center inside the flex container. Other options include:

- flex-start: aligns items to the start of the flex container. For a row, this pushes the items to the left of the container. For a column, this pushes the items to the top of the container. This is the default alignment if no justify-content is specified.
- flex-end: aligns items to the end of the flex container. For a row, this pushes the items to the right of the container. For a column this pushes the items to the bottom of the container.
- space-between: aligns items to the center of the main axis, with extra space placed between the items. The first and last items are pushed to the very edge of the flex container. In a row the first item is against the left side of the container, the last item is against the right side of the container, then the remaining space is distributed evenly among the other items.
- space-around: similar to space-between but the first and last items are not locked to the edges of the container, the space is distributed around all the items with a half space on either end of the flex container.
- space-evenly: distributes space evenly between the flex items with a full space at either end of the flex container.

The align-items property is similar to justify-content. The justify-content property aligned flex items along the main axis. For rows, the main axis is a horizontal line and for columns it is a vertical line. Flex containers also have a cross axis which is the opposite of the main axis. For rows, the cross axis is vertical and for columns, the cross axis is horizontal.

CSS offers the align-items property to align flex items along the cross axis. For a row, it tells CSS how to push the items in the entire row up or down within the container. And for a column, how to push all the items left or right within the container.

The different values available for align-items include:

- flex-start: aligns items to the start of the flex container. For rows, this aligns items to the top of the container. For columns, this aligns items to the left of the container.
- flex-end: aligns items to the end of the flex container. For rows, this aligns items to the bottom of the container. For columns, this aligns items to the right of the container.
- center: align items to the center. For rows, this vertically aligns items (equal space above and below the items). For columns, this horizontally aligns them (equal space to the left and right of the items).
- stretch: stretch the items to fill the flex container. For example, rows items are stretched to fill the flex container top-to-bottom. This is the default value if no align-items value is specified.
- baseline: align items to their baselines. Baseline is a text concept, think of it as the line that the letters sit on.

CSS flexbox has a feature to split a flex container into multiple rows (or columns). By default, a flex container will fit all flex items together. For example, a row will all be on one line. Using the flex-wrap property tells CSS to wrap items. This means extra items move into a new row or column. The break point of where the wrapping happens depends on the size of the items and the size of the container. CSS also has options for the direction of the wrap:

- nowrap: this is the default setting, and does not wrap items.
- wrap: wraps items onto multiple lines from top-to-bottom if they are in rows and left-to-right if they are in columns.
- wrap-reverse: wraps items onto multiple lines from bottom-to-top if they are in rows and right-to-left if they are in columns.

So far, all the properties apply to the flex container (the parent of the flex items). However, there are several useful properties for the flex items. The first is the flex-shrink property. When it's used, it allows an item to shrink if the flex container is too small. Items shrink when the width of the parent container is smaller than the combined widths of all the flex items within it. The flex-shrink property takes numbers as values. The higher the number, the more it will shrink compared to the other items in the container. For example, if one item has a flex-shrink value of 1 and the other has a flex-shrink value of 3, the one with the value of 3 will shrink three times as much as the other.

The opposite of flex-shrink is the flex-grow property. The flex-shrink controls the size of the items when the container shrinks. The flex-grow property controls the size of items when the parent container expands. For example, if one item has a flex-grow value of 1 and the other has a flex-grow value of 3, the one with the value of 3 will grow three times as much as the other.

The flex-basis property specifies the initial size of the item before CSS makes adjustments with flex-shrink or flex-grow. The units used by the flex-basis property are the same as other size properties (px, em, %, etc.). The value auto sizes items based on the content.

The flex-grow, flex-shrink, and flex-basis properties can all be set together by using the flex property. For example, flex: 1 0 10px; will set the item to flex-grow: 1;, flex-shrink: 0;, and flex-basis: 10px;. The default property settings are flex: 0 1 auto;.

The order property is used to tell CSS the order of how flex items appear in the flex container. By default, items will appear in the same order they come in the source HTML. The property takes numbers as values, and negative numbers can be used.

The align-self property allows to adjust each item's alignment individually, instead of setting them all at once. This is useful since other common adjustment techniques using the CSS properties float, clear, and vertical-align do not work on flex items. The align-self accepts the same values as align-items and will override any value set by the align-items property.

</details>

<details><summary>CSS Grid</summary>

Turn any HTML element into a grid container by setting its display property to grid. This gives you the ability to use all the other properties associated with CSS Grid. In CSS Grid, the parent element is referred to as the container and its children are called items.

Simply creating a grid element doesn't get you very far. You need to define the structure of the grid as well. To add some columns to the grid, use the grid-template-columns property on a grid container:

```css
.container {
  display: grid;
  grid-template-columns: 50px 50px;
}
```

The number of parameters given to the grid-template-columns property indicates the number of columns in the grid, and the value of each parameter indicates the width of each column. This grid will set the number of rows automatically. To adjust the rows manually, use the grid-template-rows property in the same way you used grid-template-columns.

```css
.container {
  display: grid;
  grid-template-rows: 50px 50px;
}
```

You can use absolute and relative units like px and em in CSS Grid to define the size of rows and columns. You can use these as well:

- fr: sets the column or row to a fraction of the available space,
- auto: sets the column or row to the width or height of its content automatically,
- %: adjusts the column or row to the percent width of its container.

```css
grid-template-columns: auto 50px 10% 2fr 1fr;
```

The first column is as wide as its content, the second column is 50px, the third column is 10% of its container, and for the last two columns; the remaining space is divided into three sections, two are allocated for the fourth column, and one for the fifth.

Sometimes you want a gap in between the columns. To add a gap between the columns, use the grid-column-gap property. This creates 10px of empty space between all of our columns. You can add a gap in between the rows of a grid using grid-row-gap in the same way that you added a gap in between columns.

```css
grid-column-gap: 10px;
grid-row-gap: 10px;
```

grid-gap is a shorthand property for grid-row-gap and grid-column-gap. If grid-gap has one value, it will create a gap between all rows and columns. However, if there are two values, it will use the first one to set the gap between the rows and the second value for the columns.

```css
grid-gap: 10px 20px;
```

Up to this point, all the properties that have been discussed are for grid containers. The grid-column property is the first one for use on the grid items themselves.

The hypothetical horizontal and vertical lines that create the grid are referred to as lines. These lines are numbered starting with 1 at the top left corner of the grid and move right for columns and down for rows, counting upward.

This is what the lines look like for a 3x3 grid:

https://www.freecodecamp.org/learn/responsive-web-design/css-grid/use-grid-column-to-control-spacing

To control the number of columns an item will consume, you can use the grid-column property in conjunction with the line numbers you want the item to start and stop at. This will make the item start at the first vertical line of the grid on the left and span to the 3rd line of the grid, consuming two columns. Of course, you can make items consume multiple rows just like you can with columns. You define the horizontal lines you want an item to start and stop at using the grid-row property on a grid item.

```css
grid-column: 1 / 3;
```

In CSS Grid, the content of each item is located in a box which is referred to as a cell. You can align the content's position within its cell horizontally using the justify-self property on a grid item. By default, this property has a value of stretch, which will make the content fill the whole width of the cell. This CSS Grid property accepts other values as well:

- start: aligns the content at the left of the cell,
- center: aligns the content in the center of the cell,
- end: aligns the content at the right of the cell.

Just as you can align an item horizontally, there's a way to align an item vertically as well. To do this, you use the align-self property on an item. This property accepts all of the same values as justify-self from the last challenge.

Sometimes you want all the items in your CSS Grid to share the same alignment. You can align them individually, or you can align them all at once horizontally by using justify-items on your grid container. This property can accept all the same values like before, the difference being that it will move all the items in our grid to the desired alignment.

Using the align-items property on a grid container will set the vertical alignment for all the items in our grid.

```css
align-items: end;
```

You can group cells of your grid together into an area and give the area a custom name by using grid-template-areas on the container. Every word represents a cell and every pair of quotation marks represent a row.

```css
grid-template-areas:
  "header header header"
  "advert content content"
  "advert footer footer";
```

After creating an area template for your grid container, you can place an item in your custom area by referencing the name you gave it. To do this, you use the grid-area property on an item.

```css
.item1 {
  grid-area: header;
}
```

This lets the grid know that you want the item1 class to go in the area named header. In this case, the item will use the entire top row because that whole row is named as the header area.

The grid-area property can be used in another way. If your grid doesn't have an areas template to reference, you can create an area on the fly for an item to be placed.

```css
.item1 {
  grid-area: 1/1/2/4;
}
```

This is using the line numbers to define where the area for this item will be. The numbers represent these values:

- grid-area: horizontal line to start at / vertical line to start at / horizontal line to end at / vertical line to end at;

So the item in the example will consume the rows between lines 1 and 2, and the columns between lines 1 and 4.

There's a better way - by using the repeat function to specify the number of times you want your column or row to be repeated, followed by a comma and the value you want to repeat. Create the 100 row grid, each row at 50px tall.

```css
grid-template-rows: repeat(100, 50px);
```

You can also repeat multiple values with the repeat function and insert the function amongst other values when defining a grid structure.

```css
grid-template-columns: repeat(2, 1fr 50px) 20px;
```

This translates to:

```css
grid-template-columns: 1fr 50px 1fr 50px 20px;
```

There's another built-in function to use with grid-template-columns and grid-template-rows called minmax. It's used to limit the size of items when the grid container changes size. To do this you need to specify the acceptable size range for your item. Here is an example:

```css
grid-template-columns: 100px minmax(50px, 200px);
```

In the code above, grid-template-columns is set to create two columns; the first is 100px wide, and the second has the minimum width of 50px and the maximum width of 200px.

The repeat function comes with an option called auto-fill. This allows you to automatically insert as many rows or columns of your desired size as possible depending on the size of the container. You can create flexible layouts when combining auto-fill with minmax.

```css
repeat(auto-fill, minmax(60px, 1fr));
```

When the container changes size, this setup keeps inserting 60px columns and stretching them until it can insert another one. If your container can't fit all your items on one row, it will move them down to a new one.

auto-fit works almost identically to auto-fill. The only difference is that when the container's size exceeds the size of all the items combined, auto-fill keeps inserting empty rows or columns and pushes your items to the side, while auto-fit collapses those empty rows or columns and stretches your items to fit the size of the container. If your container can't fit all your items on one row, it will move them down to a new one.

CSS Grid can be an easy way to make your site more responsive by using media queries to rearrange grid areas, change dimensions of a grid, and rearrange the placement of items.

```css
@media (min-width: 300px) {
  .container {
    grid-template-columns: auto 1fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
      "advert header"
      "advert content"
      "advert footer";
  }
}
```

Turning an element into a grid only affects the behavior of its direct descendants. So by turning a direct descendant into a grid, you have a grid within a grid. For example, by setting the display and grid-template-columns properties of the element with the item3 class, you create a grid within your grid.

```css
.item3 {
  background: PaleTurquoise;
  grid-area: content;
  display: grid;
  grid-template-columns: auto 1fr;
}
```

</details>

<details><summary>Responsive Web Design Projects</summary>
</details>

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

```css

```

<details><summary>Basic HTML and HTML5</summary>
</details>

1688

## JavaScript Algorithms and Data Structures Certification

<details><summary>Basic JavaScript</summary>

JavaScript is a scripting language you can use to make web pages interactive. It is one of the core technologies of the web, along with HTML and CSS, and is supported by all modern browsers.

In this course, you'll learn fundamental programming concepts in JavaScript. You'll start with basic data structures like numbers and strings. Then you'll learn to work with arrays, objects, functions, loops, if/else statements, and more.

Comments are lines of code that JavaScript will intentionally ignore. Comments are a great way to leave notes to yourself and to other people who will later need to figure out what that code does.

There are two ways to write comments in JavaScript:

Using // will tell JavaScript to ignore the remainder of the text on the current line. This is an in-line comment:

// This is an in-line comment.
You can make a multi-line comment beginning with /_ and ending with _/. This is a multi-line comment:

/_ This is a
multi-line comment _/

NOTE: As you write code, you should regularly add comments to clarify the function of parts of your code. Good commenting can help communicate the intent of your code—both for others and for your future self.

In computer science, data is anything that is meaningful to the computer. JavaScript provides eight different data types which are undefined, null, boolean, string, symbol, bigint, number, and object.

For example, computers distinguish between numbers, such as the number 12, and strings, such as "12", "dog", or "123 cats", which are collections of characters. Computers can perform mathematical operations on a number, but not on a string.

Variables allow computers to store and manipulate data in a dynamic fashion. They do this by using a "label" to point to the data rather than using the data itself. Any of the eight data types may be stored in a variable.

Variables are similar to the x and y variables you use in mathematics, which means they're a simple name to represent the data we want to refer to. Computer variables differ from mathematical variables in that they can store different values at different times.

We tell JavaScript to create or declare a variable by putting the keyword var in front of it, like so:

var ourName;

creates a variable called ourName. In JavaScript we end statements with semicolons. Variable names can be made up of numbers, letters, and $ or \_, but may not contain spaces or start with a number.

In JavaScript, you can store a value in a variable with the assignment operator (=).

myVariable = 5;
This assigns the Number value 5 to myVariable.

If there are any calculations to the right of the = operator, those are performed before the value is assigned to the variable on the left of the operator.

var myVar;
myVar = 5;

First, this code creates a variable named myVar. Then, the code assigns 5 to myVar. Now, if myVar appears again in the code, the program will treat it as if it is 5.

After a value is assigned to a variable using the assignment operator, you can assign the value of that variable to another variable using the assignment operator.

var myVar;
myVar = 5;
var myNum;
myNum = myVar;

The above declares a myVar variable with no value, then assigns it the value 5. Next, a variable named myNum is declared with no value. Then, the contents of myVar (which is 5) is assigned to the variable myNum. Now, myNum also has the value of 5.

It is common to initialize a variable to an initial value in the same line as it is declared.

var myVar = 0;

Creates a new variable called myVar and assigns it an initial value of 0.

Previously you used the following code to declare a variable:

var myName;

But you can also declare a string variable like this:

var myName = "your name";

"your name" is called a string literal. A string literal, or string, is a series of zero or more characters enclosed in single or double quotes.

When JavaScript variables are declared, they have an initial value of undefined. If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". If you concatenate a string with an undefined variable, you will get a string of undefined.

In JavaScript all variables and function names are case sensitive. This means that capitalization matters.

MYVAR is not the same as MyVar nor myvar. It is possible to have multiple distinct variables with the same name but different casing. It is strongly recommended that for the sake of clarity, you do not use this language feature.

Best Practice

Write variable names in JavaScript in camelCase. In camelCase, multi-word variable names have the first word in lowercase and the first letter of each subsequent word is capitalized.

Examples:

var someVariable;
var anotherVariableName;
var thisVariableNameIsSoLong;

One of the biggest problems with declaring variables with the var keyword is that you can easily overwrite variable declarations:

var camper = "James";
var camper = "David";
console.log(camper);

In the code above, the camper variable is originally declared as James, and is then overridden to be David. The console then displays the string David.

In a small application, you might not run into this type of problem. But as your codebase becomes larger, you might accidentally overwrite a variable that you did not intend to. Because this behavior does not throw an error, searching for and fixing bugs becomes more difficult.

A keyword called let was introduced in ES6, a major update to JavaScript, to solve this potential issue with the var keyword. You'll learn about other ES6 features in later challenges.

If you replace var with let in the code above, it results in an error:

let camper = "James";
let camper = "David";

The error can be seen in your browser console.

So unlike var, when you use let, a variable with the same name can only be declared once.

The keyword let is not the only new way to declare variables. In ES6, you can also declare variables using the const keyword.

const has all the awesome features that let has, with the added bonus that variables declared using const are read-only. They are a constant value, which means that once a variable is assigned with const, it cannot be reassigned:

const FAV_PET = "Cats";
FAV_PET = "Dogs";

The console will display an error due to reassigning the value of FAV_PET.

You should always name variables you don't want to reassign using the const keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant.

Note: It is common for developers to use uppercase variable identifiers for immutable values and lowercase or camelCase for mutable values (objects and arrays). You will learn more about objects, arrays, and immutable and mutable values in later challenges. Also in later challenges, you will see examples of uppercase, lowercase, or camelCase variable identifiers. Use let when you want the variable to change, and const when you want the variable to remain constant.

Number is a data type in JavaScript which represents numeric data.

Now let's try to add two numbers using JavaScript.

JavaScript uses the + symbol as an addition operator when placed between two numbers.

Example:

const myVar = 5 + 10;

myVar now has the value 15.

We can also subtract one number from another.

JavaScript uses the - symbol for subtraction.

Example

const myVar = 12 - 6;

myVar would have the value 6.

We can also multiply one number by another.

JavaScript uses the \* symbol for multiplication of two numbers.

Example

const myVar = 13 \* 13;

myVar would have the value 169.

We can also divide one number by another.

JavaScript uses the / symbol for division.

Example

const myVar = 16 / 2;

myVar now has the value 8.

You can easily increment or add one to a variable with the ++ operator.

i++;
is the equivalent of

i = i + 1;
Note: The entire line becomes i++;, eliminating the need for the equal sign.

You can easily decrement or decrease a variable by one with the -- operator.

i--;
is the equivalent of

i = i - 1;
Note: The entire line becomes i--;, eliminating the need for the equal sign.

We can store decimal numbers in variables too. Decimal numbers are sometimes referred to as floating point numbers or floats.

Note: Not all real numbers can accurately be represented in floating point. This can lead to rounding errors.

https://en.wikipedia.org/wiki/Floating-point_arithmetic#Accuracy_problems

In JavaScript, you can also perform calculations with decimal numbers, just like whole numbers.

Let's multiply two decimals together to get their product.

Now let's divide one decimal by another.

The remainder operator % gives the remainder of the division of two numbers.

Example

5 % 2 = 1 because
Math.floor(5 / 2) = 2 (Quotient)
2 \* 2 = 4
5 - 4 = 1 (Remainder)
Usage
In mathematics, a number can be checked to be even or odd by checking the remainder of the division of the number by 2.

17 % 2 = 1 (17 is Odd)
48 % 2 = 0 (48 is Even)
Note: The remainder operator is sometimes incorrectly referred to as the modulus operator. It is very similar to modulus, but does not work properly with negative numbers.

In programming, it is common to use assignments to modify the contents of a variable. Remember that everything to the right of the equals sign is evaluated first, so we can say:

myVar = myVar + 5;
to add 5 to myVar. Since this is such a common pattern, there are operators which do both a mathematical operation and assignment in one step.

One such operator is the += operator.

let myVar = 1;
myVar += 5;
console.log(myVar);
6 would be displayed in the console.

Like the += operator, -= subtracts a number from a variable.

myVar = myVar - 5;
will subtract 5 from myVar. This can be rewritten as:

myVar -= 5;

The \*= operator multiplies a variable by a number.

myVar = myVar \* 5;
will multiply myVar by 5. This can be rewritten as:

myVar \*= 5;

The /= operator divides a variable by another number.

myVar = myVar / 5;
Will divide myVar by 5. This can be rewritten as:

myVar /= 5;

When you are defining a string you must start and end with a single or double quote. What happens when you need a literal quote: " or ' inside of your string?

In JavaScript, you can escape a quote from considering it as an end of string quote by placing a backslash (\) in front of the quote.

const sampleStr = "Alan said, \"Peter is learning JavaScript\".";

This signals to JavaScript that the following quote is not the end of the string, but should instead appear inside the string. So if you were to print this to the console, you would get:

Alan said, "Peter is learning JavaScript".
Use backslashes to assign a string to the myStr variable so that if you were to print it to the console, you would see:

I am a "double quoted" string inside "double quotes".

String values in JavaScript may be written with single or double quotes, as long as you start and end with the same type of quote. Unlike some other programming languages, single and double quotes work the same in JavaScript.

const doubleQuoteStr = "This is a string";
const singleQuoteStr = 'This is also a string';

The reason why you might want to use one type of quote over the other is if you want to use both in a string. This might happen if you want to save a conversation in a string and have the conversation in quotes. Another use for it would be saving an <a> tag with various attributes in quotes, all within a string.

const conversation = 'Finn exclaims to Jake, "Algebraic!"';

However, this becomes a problem if you need to use the outermost quotes within it. Remember, a string has the same kind of quote at the beginning and end. But if you have that same quote somewhere in the middle, the string will stop early and throw an error.

const goodStr = 'Jake asks Finn, "Hey, let\'s go on an adventure?"';
const badStr = 'Finn responds, "Let's go!"';

Here badStr will throw an error.

In the goodStr above, you can use both quotes safely by using the backslash \ as an escape character.

Note: The backslash \ should not be confused with the forward slash /. They do not do the same thing.

Quotes are not the only characters that can be escaped inside a string. There are two reasons to use escaping characters:

To allow you to use characters you may not otherwise be able to type out, such as a carriage return.
To allow you to represent multiple quotes in a string without JavaScript misinterpreting what you mean.
We learned this in the previous challenge.

Code Output
\' single quote
\" double quote
\\ backslash
\n newline
\r carriage return
\t tab
\b word boundary
\f form feed

Note that the backslash itself must be escaped in order to display as a backslash.

In JavaScript, when the + operator is used with a String value, it is called the concatenation operator. You can build a new string out of other strings by concatenating them together.

Example

'My name is Alan,' + ' I concatenate.'

Note: Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

Example:

const ourStr = "I come first. " + "I come second.";

The string I come first. I come second. would be displayed in the console.

We can also use the += operator to concatenate a string onto the end of an existing string variable. This can be very helpful to break a long string over several lines.

Note: Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

Example:

let ourStr = "I come first. ";
ourStr += "I come second.";
ourStr now has a value of the string I come first. I come second..

Sometimes you will need to build a string, Mad Libs style. By using the concatenation operator (+), you can insert one or more variables into a string you're building.

https://en.wikipedia.org/wiki/Mad_Libs

Example:

const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";
ourStr would have a value of the string Hello, our name is freeCodeCamp, how are you?.

Just as we can build a string over multiple lines out of string literals, we can also append variables to a string using the plus equals (+=) operator.

Example:

const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;
ourStr would have the value freeCodeCamp is awesome!.

You can find the length of a String value by writing .length after the string variable or string literal.

console.log("Alan Peter".length);
The value 10 would be displayed in the console. Note that the space character between "Alan" and "Peter" is also counted.

For example, if we created a variable const firstName = "Ada", we could find out how long the string Ada is by using the firstName.length property.

Bracket notation is a way to get a character at a specific index within a string.

Most modern programming languages, like JavaScript, don't start counting at 1 like humans do. They start at 0. This is referred to as Zero-based indexing.

For example, the character at index 0 in the word Charles is C. So if const firstName = "Charles", you can get the value of the first letter of the string by using firstName[0].

Example:

const firstName = "Charles";
const firstLetter = firstName[0];
firstLetter would have a value of the string C.

In JavaScript, String values are immutable, which means that they cannot be altered once created.

For example, the following code:

let myStr = "Bob";
myStr[0] = "J";

cannot change the value of myStr to Job, because the contents of myStr cannot be altered. Note that this does not mean that myStr cannot be changed, just that the individual characters of a string literal cannot be changed. The only way to change myStr would be to assign it with a new string, like this:

let myStr = "Bob";
myStr = "Job";

You can also use bracket notation to get the character at other positions within a string.

Remember that computers start counting at 0, so the first character is actually the zeroth character.

Example:

const firstName = "Ada";
const secondLetterOfFirstName = firstName[1];
secondLetterOfFirstName would have a value of the string d.

In order to get the last letter of a string, you can subtract one from the string's length.

For example, if const firstName = "Ada", you can get the value of the last letter of the string by using firstName[firstName.length - 1].

Example:

const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];

lastLetter would have a value of the string a.

You can use the same principle we just used to retrieve the last character in a string to retrieve the Nth-to-last character.

For example, you can get the value of the third-to-last letter of the const firstName = "Augusta" string by using firstName[firstName.length - 3]

Example:

const firstName = "Augusta";
const thirdToLastLetter = firstName[firstName.length - 3];
thirdToLastLetter would have a value of the string s.

We will now use our knowledge of strings to build a "Mad Libs" style word game we're calling "Word Blanks". You will create an (optionally humorous) "Fill in the Blanks" style sentence.

In a "Mad Libs" game, you are provided sentences with some missing words, like nouns, verbs, adjectives and adverbs. You then fill in the missing pieces with words of your choice in a way that the completed sentence makes sense.

Consider this sentence - It was really \_**\_, and we \_\_** ourselves \_\_\_\_. This sentence has three missing pieces- an adjective, a verb and an adverb, and we can add words of our choice to complete it. We can then assign the completed sentence to a variable as follows:

const sentence = "It was really " + "hot" + ", and we " + "laughed" + " ourselves " + "silly" + ".";

With JavaScript array variables, we can store several pieces of data in one place.

You start an array declaration with an opening square bracket, end it with a closing square bracket, and put a comma between each entry, like this:

const sandwich = ["peanut butter", "jelly", "bread"];

You can also nest arrays within other arrays, like below:

const teams = [["Bulls", 23], ["White Sox", 45]];
This is also called a multi-dimensional array.

We can access the data inside arrays using indexes.

Array indexes are written in the same bracket notation that strings use, except that instead of specifying a character, they are specifying an entry in the array. Like strings, arrays use zero-based indexing, so the first element in an array has an index of 0.

Example

const array = [50, 60, 70];
console.log(array[0]);
const data = array[1];

The console.log(array[0]) prints 50, and data has the value 60.

Unlike strings, the entries of arrays are mutable and can be changed freely, even if the array was declared with const.

Example

const ourArray = [50, 40, 30];
ourArray[0] = 15;

ourArray now has the value [15, 40, 30].

Note: There shouldn't be any spaces between the array name and the square brackets, like array [0]. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

One way to think of a multi-dimensional array, is as an array of arrays. When you use brackets to access your array, the first set of brackets refers to the entries in the outer-most (the first level) array, and each additional pair of brackets refers to the next level of entries inside.

Example

const arr = [
[1, 2, 3],
[4, 5, 6],
[7, 8, 9],
[[10, 11, 12], 13, 14]
];

arr[3];
arr[3][0];
arr[3][0][1];
arr[3] is [[10, 11, 12], 13, 14], arr[3][0] is [10, 11, 12], and arr[3][0][1] is 11.

Note: There shouldn't be any spaces between the array name and the square brackets, like array [0][0] and even this array [0] [0] is not allowed. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

An easy way to append data to the end of an array is via the push() function.

.push() takes one or more parameters and "pushes" them onto the end of the array.

Examples:

const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
arr1 now has the value [1, 2, 3, 4] and arr2 has the value ["Stimpson", "J", "cat", ["happy", "joy"]].

Another way to change the data in an array is with the .pop() function.

.pop() is used to pop a value off of the end of an array. We can store this popped off value by assigning it to a variable. In other words, .pop() removes the last element from an array and returns that element.

Any type of entry can be popped off of an array - numbers, strings, even nested arrays.

const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);

The first console.log will display the value 6, and the second will display the value [1, 4].

pop() always removes the last element of an array. What if you want to remove the first?

That's where .shift() comes in. It works just like .pop(), except it removes the first element instead of the last.

Example:

const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();

removedFromOurArray would have a value of the string Stimpson, and ourArray would have ["J", ["cat"]].

Not only can you shift elements off of the beginning of an array, you can also unshift elements to the beginning of an array i.e. add elements in front of the array.

.unshift() works exactly like .push(), but instead of adding the element at the end of the array, unshift() adds the element at the beginning of the array.

Example:

const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
After the shift, ourArray would have the value ["J", "cat"]. After the unshift, ourArray would have the value ["Happy", "J", "cat"].

In JavaScript, we can divide up our code into reusable parts called functions.

Here's an example of a function:

function functionName() {
console.log("Hello World");
}
You can call or invoke this function by using its name followed by parentheses, like this: functionName(); Each time the function is called it will print out the message Hello World on the dev console. All of the code between the curly braces will be executed every time the function is called.

Parameters are variables that act as placeholders for the values that are to be input to a function when it is called. When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as arguments.

Here is a function with two parameters, param1 and param2:

function testFun(param1, param2) {
console.log(param1, param2);
}
Then we can call testFun like this: testFun("Hello", "World");. We have passed two string arguments, Hello and World. Inside the function, param1 will equal the string Hello and param2 will equal the string World. Note that you could call testFun again with different arguments and the parameters would take on the value of the new arguments.

We can pass values into a function with arguments. You can use a return statement to send a value back out of a function.

Example

function plusThree(num) {
return num + 3;
}

const answer = plusThree(5);
answer has the value 8.

plusThree takes an argument for num and returns a value equal to num + 3.

In JavaScript, scope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code.

Variables which are declared without the let or const keywords are automatically created in the global scope. This can create unintended consequences elsewhere in your code or when running a function again. You should always declare your variables with let or const.

const myGlobal = 10;

function fun1() {
oopsGlobal = 5;
}

function fun2() {
var output = "";
if (typeof myGlobal != "undefined") {
output += "myGlobal: " + myGlobal;
}
if (typeof oopsGlobal != "undefined") {
output += " oopsGlobal: " + oopsGlobal;
}
console.log(output);
}

Variables which are declared within a function, as well as the function parameters, have local scope. That means they are only visible within that function.

Here is a function myTest with a local variable called loc.

function myTest() {
const loc = "foo";
console.log(loc);
}

myTest();
console.log(loc);

The myTest() function call will display the string foo in the console. The console.log(loc) line (outside of the myTest function) will throw an error, as loc is not defined outside of the function.

It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable.

In this example:

const someVar = "Hat";

function myFun() {
const someVar = "Head";
return someVar;
}
The function myFun will return the string Head because the local version of the variable is present.

A function can include the return statement but it does not have to. In the case that the function doesn't have a return statement, when you call it, the function processes the inner code but the returned value is undefined.

Example

let sum = 0;

function addSum(num) {
sum = sum + num;
}

addSum(3);
addSum is a function without a return statement. The function will change the global sum variable but the returned value of the function is undefined.

If you'll recall from our discussion of Storing Values with the Assignment Operator, everything to the right of the equal sign is resolved before the value is assigned. This means we can take the return value of a function and assign it to a variable.

Assume we have pre-defined a function sum which adds two numbers together, then:

ourSum = sum(5, 12);
will call the sum function, which returns a value of 17 and assigns it to the ourSum variable.

In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

function nextInLine(arr, item) {
arr.push(item);
const firstItem = arr.shift();
return firstItem;
}

const testArr = [1, 2, 3, 4, 5];

console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));

Another data type is the Boolean. Booleans may only be one of two values: true or false. They are basically little on-off switches, where true is on and false is off. These two states are mutually exclusive.

Note: Boolean values are never written with quotes. The strings "true" and "false" are not Boolean and have no special meaning in JavaScript.

function welcomeToBooleans() {
// Only change code below this line

return true; // Change this line

// Only change code above this line
}

if statements are used to make decisions in code. The keyword if tells JavaScript to execute the code in the curly braces under certain conditions, defined in the parentheses. These conditions are known as Boolean conditions and they may only be true or false.

When the condition evaluates to true, the program executes the statement inside the curly braces. When the Boolean condition evaluates to false, the statement inside the curly braces will not execute.

Pseudocode

if (condition is true) {
statement is executed
}

Example

function test (myCondition) {
if (myCondition) {
return "It was true";
}
return "It was false";
}

test(true);
test(false);

test(true) returns the string It was true, and test(false) returns the string It was false.

When test is called with a value of true, the if statement evaluates myCondition to see if it is true or not. Since it is true, the function returns It was true. When we call test with a value of false, myCondition is not true and the statement in the curly braces is not executed and the function returns It was false.

There are many comparison operators in JavaScript. All of these operators return a boolean true or false value.

The most basic operator is the equality operator ==. The equality operator compares two values and returns true if they're equivalent or false if they are not. Note that equality is different from assignment (=), which assigns the value on the right of the operator to a variable on the left.

function equalityTest(myVal) {
if (myVal == 10) {
return "Equal";
}
return "Not Equal";
}
If myVal is equal to 10, the equality operator returns true, so the code in the curly braces will execute, and the function will return Equal. Otherwise, the function will return Not Equal. In order for JavaScript to compare two different data types (for example, numbers and strings), it must convert one type to another. This is known as Type Coercion. Once it does, however, it can compare terms as follows:

1 == 1 // true
1 == 2 // false
1 == '1' // true
"3" == 3 // true

Strict equality (===) is the counterpart to the equality operator (==). However, unlike the equality operator, which attempts to convert both values being compared to a common type, the strict equality operator does not perform a type conversion.

If the values being compared have different types, they are considered unequal, and the strict equality operator will return false.

Examples

3 === 3 // true
3 === '3' // false
In the second example, 3 is a Number type and '3' is a String type.

In the last two challenges, we learned about the equality operator (==) and the strict equality operator (===). Let's do a quick review and practice using these operators some more.

If the values being compared are not of the same type, the equality operator will perform a type conversion, and then evaluate the values. However, the strict equality operator will compare both the data type and value as-is, without converting one type to the other.

Examples

3 == '3' returns true because JavaScript performs type conversion from string to number. 3 === '3' returns false because the types are different and type conversion is not performed.

Note: In JavaScript, you can determine the type of a variable or a value with the typeof operator, as follows:

typeof 3
typeof '3'
typeof 3 returns the string number, and typeof '3' returns the string string.

function compareEquality(a, b) {
if (a === b) { // Change this line
return "Equal";
}
return "Not Equal";
}

compareEquality(10, "10");

The inequality operator (!=) is the opposite of the equality operator. It means not equal and returns false where equality would return true and vice versa. Like the equality operator, the inequality operator will convert data types of values while comparing.

Examples

1 != 2 // true
1 != "1" // false
1 != '1' // false
1 != true // false
0 != false // false

The strict inequality operator (!==) is the logical opposite of the strict equality operator. It means "Strictly Not Equal" and returns false where strict equality would return true and vice versa. The strict inequality operator will not convert data types.

Examples

3 !== 3 // false
3 !== '3' // true
4 !== 3 // true

The greater than operator (>) compares the values of two numbers. If the number to the left is greater than the number to the right, it returns true. Otherwise, it returns false.

Like the equality operator, the greater than operator will convert data types of values while comparing.

Examples

5 > 3 // true
7 > '3' // true
2 > 3 // false
'1' > 9 // false

The greater than or equal to operator (>=) compares the values of two numbers. If the number to the left is greater than or equal to the number to the right, it returns true. Otherwise, it returns false.

Like the equality operator, the greater than or equal to operator will convert data types while comparing.

Examples

6 >= 6 // true
7 >= '3' // true
2 >= 3 // false
'7' >= 9 // false

The less than operator (<) compares the values of two numbers. If the number to the left is less than the number to the right, it returns true. Otherwise, it returns false. Like the equality operator, the less than operator converts data types while comparing.

Examples

2 < 5 // true
'3' < 7 // true
5 < 5 // false
3 < 2 // false
'8' < 4 // false

The less than or equal to operator (<=) compares the values of two numbers. If the number to the left is less than or equal to the number to the right, it returns true. If the number on the left is greater than the number on the right, it returns false. Like the equality operator, the less than or equal to operator converts data types.

Examples

4 <= 5 // true
'7' <= 7 // true
5 <= 5 // true
3 <= 2 // false
'8' <= 4 // false

Sometimes you will need to test more than one thing at a time. The logical and operator (&&) returns true if and only if the operands to the left and right of it are true.

The same effect could be achieved by nesting an if statement inside another if:

if (num > 5) {
if (num < 10) {
return "Yes";
}
}
return "No";

will only return Yes if num is greater than 5 and less than 10. The same logic can be written as:

if (num > 5 && num < 10) {
return "Yes";
}
return "No";

The logical or operator (||) returns true if either of the operands is true. Otherwise, it returns false.

The logical or operator is composed of two pipe symbols: (||). This can typically be found between your Backspace and Enter keys.

The pattern below should look familiar from prior waypoints:

if (num > 10) {
return "No";
}
if (num < 5) {
return "No";
}
return "Yes";

will return Yes only if num is between 5 and 10 (5 and 10 included). The same logic can be written as:

if (num > 10 || num < 5) {
return "No";
}
return "Yes";

When a condition for an if statement is true, the block of code following it is executed. What about when that condition is false? Normally nothing would happen. With an else statement, an alternate block of code can be executed.

if (num > 10) {
return "Bigger than 10";
} else {
return "10 or Less";
}

If you have multiple conditions that need to be addressed, you can chain if statements together with else if statements.

if (num > 15) {
return "Bigger than 15";
} else if (num < 5) {
return "Smaller than 5";
} else {
return "Between 5 and 15";
}

Order is important in if, else if statements.

The function is executed from top to bottom so you will want to be careful of what statement comes first.

Take these two functions as an example.

Here's the first:

function foo(x) {
if (x < 1) {
return "Less than one";
} else if (x < 2) {
return "Less than two";
} else {
return "Greater than or equal to two";
}
}

And the second just switches the order of the statements:

function bar(x) {
if (x < 2) {
return "Less than two";
} else if (x < 1) {
return "Less than one";
} else {
return "Greater than or equal to two";
}
}

While these two functions look nearly identical if we pass a number to both we get different outputs.

foo(0)
bar(0)

foo(0) will return the string Less than one, and bar(0) will return the string Less than two.

if/else statements can be chained together for complex logic. Here is pseudocode of multiple chained if / else if statements:

if (condition1) {
statement1
} else if (condition2) {
statement2
} else if (condition3) {
statement3
. . .
} else {
statementN
}

In the game of golf, each hole has a par, meaning, the average number of strokes a golfer is expected to make in order to sink the ball in the hole to complete the play. Depending on how far above or below par your strokes are, there is a different nickname.

Your function will be passed par and strokes arguments. Return the correct string according to this table which lists the strokes in order of priority; top (highest) to bottom (lowest):

Strokes Return
1 "Hole-in-one!"
<= par - 2 "Eagle"
par - 1 "Birdie"
par "Par"
par + 1 "Bogey"
par + 2 "Double Bogey"

> = par + 3 "Go Home!"

par and strokes will always be numeric and positive. We have added an array of all the names for your convenience.

const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

function golfScore(par, strokes) {
if (strokes === 1) return names[0];
else if (strokes <= par - 2) return names[1];
else if (strokes === par - 1 ) return names[2];
else if (strokes === par ) return names[3];
else if (strokes === par + 1 ) return names[4];
else if (strokes === par + 2 ) return names[5];
else if (strokes >= par + 3) return names[6];
}

golfScore(5, 4);

If you have many options to choose from, use a switch statement. A switch statement tests a value and can have many case statements which define various possible values. Statements are executed from the first matched case value until a break is encountered.

Here is an example of a switch statement:

switch(lowercaseLetter) {
case "a":
console.log("A");
break;
case "b":
console.log("B");
break;
}
case values are tested with strict equality (===). The break tells JavaScript to stop executing statements. If the break is omitted, the next statement will be executed.

In a switch statement you may not be able to specify all possible values as case statements. Instead, you can add the default statement which will be executed if no matching case statements are found. Think of it like the final else statement in an if/else chain.

A default statement should be the last case.

switch (num) {
case value1:
statement1;
break;
case value2:
statement2;
break;
...
default:
defaultStatement;
break;
}

If the break statement is omitted from a switch statement's case, the following case statement(s) are executed until a break is encountered. If you have multiple inputs with the same output, you can represent them in a switch statement like this:

let result = "";
switch(val) {
case 1:
case 2:
case 3:
result = "1, 2, or 3";
break;
case 4:
result = "4 alone";
}
Cases for 1, 2, and 3 will all produce the same result.

If you have many options to choose from, a switch statement can be easier to write than many chained if/else if statements. The following:

if (val === 1) {
answer = "a";
} else if (val === 2) {
answer = "b";
} else {
answer = "c";
}
can be replaced with:

switch(val) {
case 1:
answer = "a";
break;
case 2:
answer = "b";
break;
default:
answer = "c";
}

You may recall from Comparison with the Equality Operator that all comparison operators return a boolean true or false value.

Sometimes people use an if/else statement to do a comparison, like this:

function isEqual(a, b) {
if (a === b) {
return true;
} else {
return false;
}
}
But there's a better way to do this. Since === returns true or false, we can return the result of the comparison:

function isEqual(a, b) {
return a === b;
}

When a return statement is reached, the execution of the current function stops and control returns to the calling location.

Example

function myFun() {
console.log("Hello");
return "World";
console.log("byebye")
}
myFun();
The above will display the string Hello in the console, and return the string World. The string byebye will never display in the console, because the function exits at the return statement.

In the casino game Blackjack, a player can gain an advantage over the house by keeping track of the relative number of high and low cards remaining in the deck. This is called Card Counting.

Having more high cards remaining in the deck favors the player. Each card is assigned a value according to the table below. When the count is positive, the player should bet high. When the count is zero or negative, the player should bet low.

Count Change Cards
+1 2, 3, 4, 5, 6
0 7, 8, 9
-1 10, 'J', 'Q', 'K', 'A'
You will write a card counting function. It will receive a card parameter, which can be a number or a string, and increment or decrement the global count variable according to the card's value (see table). The function will then return a string with the current count and the string Bet if the count is positive, or Hold if the count is zero or negative. The current count and the player's decision (Bet or Hold) should be separated by a single space.

Example Outputs: -3 Hold or 5 Bet

Hint
Do NOT reset count to 0 when value is 7, 8, or 9.
Do NOT return an array.
Do NOT include quotes (single or double) in the output.

let count = 0;

function cc(card) {
// Only change code below this line

switch (card) {
case 2:
case 3:
case 4:
case 5:
case 6:
count += 1;
break;
case 10:
case "J":
case "Q":
case "K":
case "A":
count -= 1;
break;
}

if (count > 0) {
return count + " Bet";
} else {
return count + " Hold";
}

// Only change code above this line
}

cc(2); cc(3); cc(7); cc('K'); cc('A');

You may have heard the term object before.

Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called properties.

Objects are useful for storing data in a structured way, and can represent real world objects, like a cat.

Here's a sample cat object:

const cat = {
"name": "Whiskers",
"legs": 4,
"tails": 1,
"enemies": ["Water", "Dogs"]
};

In this example, all the properties are stored as strings, such as name, legs, and tails. However, you can also use numbers as properties. You can even omit the quotes for single-word string properties, as follows:

const anotherObject = {
make: "Ford",
5: "five",
"model": "focus"
};

However, if your object has any non-string properties, JavaScript will automatically typecast them as strings.

There are two ways to access the properties of an object: dot notation (.) and bracket notation ([]), similar to an array.

Dot notation is what you use when you know the name of the property you're trying to access ahead of time.

Here is a sample of using dot notation (.) to read an object's property:

const myObj = {
prop1: "val1",
prop2: "val2"
};

const prop1val = myObj.prop1;
const prop2val = myObj.prop2;
prop1val would have a value of the string val1, and prop2val would have a value of the string val2.

The second way to access the properties of an object is bracket notation ([]). If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.

However, you can still use bracket notation on object properties without spaces.

Here is a sample of using bracket notation to read an object's property:

const myObj = {
"Space Name": "Kirk",
"More Space": "Spock",
"NoSpace": "USS Enterprise"
};

myObj["Space Name"];
myObj['More Space'];
myObj["NoSpace"];

myObj["Space Name"] would be the string Kirk, myObj['More Space'] would be the string Spock, and myObj["NoSpace"] would be the string USS Enterprise.

Note that property names with spaces in them must be in quotes (single or double).

Another use of bracket notation on objects is to access a property which is stored as the value of a variable. This can be very useful for iterating through an object's properties or when accessing a lookup table.

Here is an example of using a variable to access a property:

const dogs = {
Fido: "Mutt",
Hunter: "Doberman",
Snoopie: "Beagle"
};

const myDog = "Hunter";
const myBreed = dogs[myDog];
console.log(myBreed);

The string Doberman would be displayed in the console.

Another way you can use this concept is when the property's name is collected dynamically during the program execution, as follows:

const someObj = {
propName: "John"
};

function propPrefix(str) {
const s = "prop";
return s + str;
}

const someProp = propPrefix("Name");
console.log(someObj[someProp]);

someProp would have a value of the string propName, and the string John would be displayed in the console.

Note that we do not use quotes around the variable name when using it to access the property because we are using the value of the variable, not the name.

After you've created a JavaScript object, you can update its properties at any time just like you would update any other variable. You can use either dot or bracket notation to update.

For example, let's look at ourDog:

const ourDog = {
"name": "Camper",
"legs": 4,
"tails": 1,
"friends": ["everything!"]
};

Since he's a particularly happy dog, let's change his name to the string Happy Camper. Here's how we update his object's name property: ourDog.name = "Happy Camper"; or ourDog["name"] = "Happy Camper"; Now when we evaluate ourDog.name, instead of getting Camper, we'll get his new name, Happy Camper.

You can add new properties to existing JavaScript objects the same way you would modify them.

Here's how we would add a bark property to ourDog:

ourDog.bark = "bow-wow";

or

ourDog["bark"] = "bow-wow";

Now when we evaluate ourDog.bark, we'll get his bark, bow-wow.

Example:

const ourDog = {
"name": "Camper",
"legs": 4,
"tails": 1,
"friends": ["everything!"]
};

ourDog.bark = "bow-wow";

We can also delete properties from objects like this:

delete ourDog.bark;

Example:

const ourDog = {
"name": "Camper",
"legs": 4,
"tails": 1,
"friends": ["everything!"],
"bark": "bow-wow"
};

delete ourDog.bark;

After the last line shown above, ourDog looks like:

{
"name": "Camper",
"legs": 4,
"tails": 1,
"friends": ["everything!"]
}

Objects can be thought of as a key/value storage, like a dictionary. If you have tabular data, you can use an object to lookup values rather than a switch statement or an if/else chain. This is most useful when you know that your input data is limited to a certain range.

Here is an example of a simple reverse alphabet lookup:

const alpha = {
1:"Z",
2:"Y",
3:"X",
4:"W",
...
24:"C",
25:"B",
26:"A"
};

alpha[2];
alpha[24];

const value = 2;
alpha[value];

alpha[2] is the string Y, alpha[24] is the string C, and alpha[value] is the string Y.

// Setup
function phoneticLookup(val) {
let result = "";

// Only change code below this line
const lookup = {
"alpha": "Adams",
"bravo": "Boston",
"charlie": "Chicago",
"delta": "Denver",
"echo": "Easy",
"foxtrot": "Frank"
}

result = lookup[val];

// Only change code above this line
return result;
}

phoneticLookup("charlie");

Sometimes it is useful to check if the property of a given object exists or not. We can use the .hasOwnProperty(propname) method of objects to determine if that object has the given property name. .hasOwnProperty() returns true or false if the property is found or not.

Example

const myObj = {
top: "hat",
bottom: "pants"
};

myObj.hasOwnProperty("top");
myObj.hasOwnProperty("middle");

The first hasOwnProperty returns true, while the second returns false.

function checkObj(obj, checkProp) {
if (obj.hasOwnProperty(checkProp)) return obj[checkProp];
return "Not Found";
}

Sometimes you may want to store data in a flexible Data Structure. A JavaScript object is one way to handle flexible data. They allow for arbitrary combinations of strings, numbers, booleans, arrays, functions, and objects.

Here's an example of a complex data structure:

const ourMusic = [
{
"artist": "Daft Punk",
"title": "Homework",
"release_year": 1997,
"formats": [
"CD",
"Cassette",
"LP"
],
"gold": true
}
];

This is an array which contains one object inside. The object has various pieces of metadata about an album. It also has a nested formats array. If you want to add more album records, you can do this by adding records to the top level array. Objects hold data in a property, which has a key-value format. In the example above, "artist": "Daft Punk" is a property that has a key of artist and a value of Daft Punk. JavaScript Object Notation or JSON is a related data interchange format used to store data.

{
"artist": "Daft Punk",
"title": "Homework",
"release_year": 1997,
"formats": [
"CD",
"Cassette",
"LP"
],
"gold": true
}

Note: You will need to place a comma after every object in the array, unless it is the last object in the array.

The sub-properties of objects can be accessed by chaining together the dot or bracket notation.

Here is a nested object:

const ourStorage = {
"desk": {
"drawer": "stapler"
},
"cabinet": {
"top drawer": {
"folder1": "a file",
"folder2": "secrets"
},
"bottom drawer": "soda"
}
};

ourStorage.cabinet["top drawer"].folder2;
ourStorage.desk.drawer;

ourStorage.cabinet["top drawer"].folder2 would be the string secrets, and ourStorage.desk.drawer would be the string stapler.

Use dot notation for all properties where possible, otherwise use bracket notation.

As we have seen in earlier examples, objects can contain both nested objects and nested arrays. Similar to accessing nested objects, array bracket notation can be chained to access nested arrays.

Here is an example of how to access a nested array:

const ourPets = [
{
animalType: "cat",
names: [
"Meowzer",
"Fluffy",
"Kit-Cat"
]
},
{
animalType: "dog",
names: [
"Spot",
"Bowser",
"Frankie"
]
}
];

ourPets[0].names[1];
ourPets[1].names[0];

ourPets[0].names[1] would be the string Fluffy, and ourPets[1].names[0] would be the string Spot.

You are given an object literal representing a part of your musical album collection. Each album has a unique id number as its key and several other properties. Not all albums have complete information.

You start with an updateRecords function that takes an object literal, records, containing the musical album collection, an id, a prop (like artist or tracks), and a value. Complete the function using the rules below to modify the object passed to the function.

Your function must always return the entire record collection object.
If prop isn't tracks and value isn't an empty string, update or set that album's prop to value.
If prop is tracks but the album doesn't have a tracks property, create an empty array and add value to it.
If prop is tracks and value isn't an empty string, add value to the end of the album's existing tracks array.
If value is an empty string, delete the given prop property from the album.
Note: A copy of the recordCollection object is used for the tests.

// Setup
const recordCollection = {
2548: {
albumTitle: 'Slippery When Wet',
artist: 'Bon Jovi',
tracks: ['Let It Rock', 'You Give Love a Bad Name']
},
2468: {
albumTitle: '1999',
artist: 'Prince',
tracks: ['1999', 'Little Red Corvette']
},
1245: {
artist: 'Robert Palmer',
tracks: []
},
5439: {
albumTitle: 'ABBA Gold'
}
};

// Only change code below this line
function updateRecords(records, id, prop, value) {

if (prop !== "tracks" && value !== "") {
records[id][prop] = value;
} else if (prop === "tracks" && records[id].hasOwnProperty("tracks") === false) {
records[id][prop] = [value];
} else if (prop === "tracks" && value !== "") {
records[id][prop].push(value);
} else if (value === "") {
delete records[id][prop];
}

return records;
}

updateRecords(recordCollection, 5439, 'artist', 'ABBA');

You can run the same code multiple times by using a loop.

The first type of loop we will learn is called a while loop because it runs while a specified condition is true and stops once that condition is no longer true.

const ourArray = [];
let i = 0;

while (i < 5) {
ourArray.push(i);
i++;
}

In the code example above, the while loop will execute 5 times and append the numbers 0 through 4 to ourArray.

Let's try getting a while loop to work by pushing values to an array.

You can run the same code multiple times by using a loop.

The most common type of JavaScript loop is called a for loop because it runs for a specific number of times.

For loops are declared with three optional expressions separated by semicolons:

for (a; b; c), where a is the initialization statement, b is the condition statement, and c is the final expression.

The initialization statement is executed one time only before the loop starts. It is typically used to define and setup your loop variable.

The condition statement is evaluated at the beginning of every loop iteration and will continue as long as it evaluates to true. When the condition is false at the start of the iteration, the loop will stop executing. This means if the condition starts as false, your loop will never execute.

The final expression is executed at the end of each loop iteration, prior to the next condition check and is usually used to increment or decrement your loop counter.

In the following example we initialize with i = 0 and iterate while our condition i < 5 is true. We'll increment i by 1 in each loop iteration with i++ as our final expression.

const ourArray = [];

for (let i = 0; i < 5; i++) {
ourArray.push(i);
}

ourArray will now have the value [0, 1, 2, 3, 4].

For loops don't have to iterate one at a time. By changing our final-expression, we can count by even numbers.

We'll start at i = 0 and loop while i < 10. We'll increment i by 2 each loop with i += 2.

const ourArray = [];

for (let i = 0; i < 10; i += 2) {
ourArray.push(i);
}

ourArray will now contain [0, 2, 4, 6, 8]. Let's change our initialization so we can count by odd numbers.

A for loop can also count backwards, so long as we can define the right conditions.

In order to decrement by two each iteration, we'll need to change our initialization, condition, and final expression.

We'll start at i = 10 and loop while i > 0. We'll decrement i by 2 each loop with i -= 2.

const ourArray = [];

for (let i = 10; i > 0; i -= 2) {
ourArray.push(i);
}

ourArray will now contain [10, 8, 6, 4, 2]. Let's change our initialization and final expression so we can count backwards by twos to create an array of descending odd numbers.

A common task in JavaScript is to iterate through the contents of an array. One way to do that is with a for loop. This code will output each element of the array arr to the console:

const arr = [10, 9, 8, 7, 6];

for (let i = 0; i < arr.length; i++) {
console.log(arr[i]);
}

Remember that arrays have zero-based indexing, which means the last index of the array is length - 1. Our condition for this loop is i < arr.length, which stops the loop when i is equal to length. In this case the last iteration is i === 4 i.e. when i becomes equal to arr.length - 1 and outputs 6 to the console. Then i increases to 5, and the loop terminates because i < arr.length is false.

If you have a multi-dimensional array, you can use the same logic as the prior waypoint to loop through both the array and any sub-arrays. Here is an example:

const arr = [
[1, 2], [3, 4], [5, 6]
];

for (let i = 0; i < arr.length; i++) {
for (let j = 0; j < arr[i].length; j++) {
console.log(arr[i][j]);
}
}

This outputs each sub-element in arr one at a time. Note that for the inner loop, we are checking the .length of arr[i], since arr[i] is itself an array.

The next type of loop you will learn is called a do...while loop. It is called a do...while loop because it will first do one pass of the code inside the loop no matter what, and then continue to run the loop while the specified condition evaluates to true.

const ourArray = [];
let i = 0;

do {
ourArray.push(i);
i++;
} while (i < 5);

The example above behaves similar to other types of loops, and the resulting array will look like [0, 1, 2, 3, 4]. However, what makes the do...while different from other loops is how it behaves when the condition fails on the first check. Let's see this in action: Here is a regular while loop that will run the code in the loop as long as i < 5:

const ourArray = [];
let i = 5;

while (i < 5) {
ourArray.push(i);
i++;
}

In this example, we initialize the value of ourArray to an empty array and the value of i to 5. When we execute the while loop, the condition evaluates to false because i is not less than 5, so we do not execute the code inside the loop. The result is that ourArray will end up with no values added to it, and it will still look like [] when all of the code in the example above has completed running. Now, take a look at a do...while loop:

const ourArray = [];
let i = 5;

do {
ourArray.push(i);
i++;
} while (i < 5);

In this case, we initialize the value of i to 5, just like we did with the while loop. When we get to the next line, there is no condition to evaluate, so we go to the code inside the curly braces and execute it. We will add a single element to the array and then increment i before we get to the condition check. When we finally evaluate the condition i < 5 on the last line, we see that i is now 6, which fails the conditional check, so we exit the loop and are done. At the end of the above example, the value of ourArray is [5]. Essentially, a do...while loop ensures that the code inside the loop will run at least once. Let's try getting a do...while loop to work by pushing values to an array.

Recursion is the concept that a function can be expressed in terms of itself. To help understand this, start by thinking about the following task: multiply the first n elements of an array to create the product of those elements. Using a for loop, you could do this:

function multiply(arr, n) {
let product = 1;
for (let i = 0; i < n; i++) {
product \*= arr[i];
}
return product;
}

However, notice that multiply(arr, n) == multiply(arr, n - 1) \* arr[n - 1]. That means you can rewrite multiply in terms of itself and never need to use a loop.

function multiply(arr, n) {
if (n <= 0) {
return 1;
} else {
return multiply(arr, n - 1) \* arr[n - 1];
}
}

The recursive version of multiply breaks down like this. In the base case, where n <= 0, it returns 1. For larger values of n, it calls itself, but with n - 1. That function call is evaluated in the same way, calling multiply again until n <= 0. At this point, all the functions can return and the original multiply returns the answer.

Note: Recursive functions must have a base case when they return without calling the function again (in this example, when n <= 0), otherwise they can never finish executing.

</details>

<details><summary>ES6</summary>
</details>

<details><summary>Regular Expressions</summary>
</details>

<details><summary>Debugging</summary>
</details>

<details><summary>Basic Data Structures</summary>
</details>

<details><summary>Basic Algorithm Scripting</summary>
</details>

<details><summary>Object Oriented Programming</summary>
</details>

<details><summary>Functional Programming</summary>
</details>

<details><summary>Intermediate Algorithm Scripting</summary>
</details>

<details><summary>JavaScript Algorithms and Data Structures Projects</summary>
</details>
