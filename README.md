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

Classes are reusable styles that can be added to HTML elements. Classes allow you to use the same CSS styles on multiple HTML elements. Class declaration:

```css
<style>
  .blue-text {
    color: blue;
  }
</style>
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

<style>
  .larger-image {
    width: 500px;
  }
</style>

CSS borders have properties like style, color and width.

```css
<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
  }
</style>
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

In addition to classes, each HTML element can also have an id attribute.

There are several benefits to using id attributes: You can use an id to style a single element and you can use them to select and modify specific elements with JavaScript. id attributes should be unique. Browsers won't enforce this, but it is a widely agreed upon best practice. Don't give more than one element the same id attribute.

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

8888888888888888888

The last several challenges all set an element's margin or padding with pixels (px). Pixels are a type of length unit, which is what tells the browser how to size or space an item. In addition to px, CSS has a number of different length unit options that you can use.

The two main types of length units are absolute and relative. Absolute units tie to physical units of length. For example, in and mm refer to inches and millimeters, respectively. Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.

Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font. If you use it to set the font-size property itself, it's relative to the parent's font-size.

Note: There are several relative unit options that are tied to the size of the viewport. They are covered in the Responsive Web Design Principles section.

Now let's start fresh and talk about CSS inheritance.

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

  </details>

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

```css

```

<details><summary>Basic HTML and HTML5</summary>
</details>
