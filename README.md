# Notebook
My personal notebook.

<details><summary>HTML</summary>
  
  HTML is a markup language that uses a special syntax or notation to describe the structure of a webpage to the browser. HTML elements usually have opening and closing tags that surround and give meaning to content. For example, different elements can describe text as a heading, paragraph, or list item.
  
  <h1>Hello</h1> - HTML element (most of them have an opening tag and a closing tag)
  <h1> - opening tag
  </h1> - closing tag
  
  <h1></h1> - main heading
  <h2></h2> - subheading
  From <h3> to <h6> - different levels of subheadings
  
  <p>I'm a p tag!</p> - preferred element for paragraph
  
  As a convention, all HTML tags are written in lowercase, for example <p></p> and not <P></P>.
  
  lorem ipsum text - placeholder text
  
  <!-- --> - comments in HTML - you can leave comments for other developers within your code without affecting the resulting output that is displayed to the end user and also a convenient way to make code inactive without having to delete it entirely
  
  HTML5 introduces more descriptive HTML tags. These include main, header, footer, nav, video, article, section and others.
  These tags give a descriptive structure to your HTML, make your HTML easier to read, and help with Search Engine Optimization (SEO) and accessibility.
  
The main HTML5 tag helps search engines and other developers find the main content of your page.
  
  <main> 
  <h1>Hello World</h1>
  <p>Hello Paragraph</p>
</main>
  
  <img src="https://www.freecatphotoapp.com/your-image.jpg" alt="A business cat wearing a necktie."> - add image, specify source attribute
  
  img elements are self-closing. All img elements must have an alt attribute. an alt attribute is used for screen readers to improve accessibility and is displayed if the image fails to load. If the image is purely decorative, using an empty alt attribute is a best practice. Ideally the alt attribute should not contain special characters unless needed.
  
  <a href="https://www.freecodecamp.org">this links to freecodecamp.org</a> - a (anchor) elements to link to content outside of your web page. a elements need a destination web address called an href attribute. They also need anchor text. 
  
  a (anchor) elements can also be used to create internal links to jump to different sections within a webpage. To create an internal link, you assign a link's href attribute to a hash symbol # plus the value of the id attribute for the element that you want to internally link to, usually further down the page. You then need to add the same id attribute to the element you are linking to. An id is an attribute that uniquely describes an element.
  
  <a href="#contacts-header">Contacts</a>
...
<h2 id="contacts-header">Contacts</h2>
  
  the target="_blank" attribute from the anchor tag since this causes the linked document to open in a new window tab.
  
  You can nest links within other text elements.
  
  <p>
  Here's a <a target="_blank" href="https://www.freecodecamp.org"> link to www.freecodecamp.org</a> for you to follow.
</p>
  
  target is an anchor tag attribute that specifies where to open the link. The value _blank specifies to open the link in a new tab. The href is an anchor tag attribute that contains the URL address of the link:
  
  <a href=" ... " target="...">link to freecodecamp.org</a>
  
  Sometimes you want to add a elements to your website before you know where they will link.

This is also handy when you're changing the behavior of a link using JavaScript
  
  value with a #, also known as a hash symbol, to create a dead link.  href="#"
  
  You can make elements into links by nesting them within an a element.
  <a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="Three kittens running towards the camera."></a>
  
  Unordered list (bullet point style list)
  
  <ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
  
  Ordered lists (numbered lists)
  
  <ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
  
  Text field - get input from your user, input elements are self-closing.
  
  <input type="text">
  
  Text field with placeholder - Placeholder text is displayed in your input element before your user has inputted anything.
  
  <input type="text" placeholder="this is placeholder text">
  
  Form element - web forms that actually submit data to a server. You can do this by specifying an action attribute on your form element.
  
  <form action="url-where-you-want-to-submit-form-data">
  <input>
</form>
  
  Submit button to a form -  Clicking this button will send the data from your form to the URL you specified with your form's action attribute.
  
  <button type="submit">this button submits the form</button>
  
  You can require specific form fields so that your user will not be able to submit your form until he or she has filled them out.

For example, if you wanted to make a text input field required, you can just add the attribute required within your input element, like this: <input type="text" required>
  
  You can use radio buttons for questions where you want the user to only give you one answer out of multiple options
  Radio buttons are a type of input. Each of your radio buttons can be nested within its own label element. By wrapping an input element inside of a label element it will automatically associate the radio button input with the label element surrounding it. All related radio buttons should have the same name attribute to create a radio button group. By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.
  
   <label> 
  <input type="radio" name="indoor-outdoor">Indoor 
</label>
  
  It is considered best practice to set a for attribute on the label element, with a value that matches the value of the id attribute of the input element. This allows assistive technologies to create a linked relationship between the label and the related input element.
  
  <input id="indoor" type="radio" name="indoor-outdoor">
<label for="indoor">Indoor</label>
  
  We can also nest the input element within the label tags:
  
  <label for="indoor"> 
  <input id="indoor" type="radio" name="indoor-outdoor">Indoor 
</label>
  
  Forms commonly use checkboxes for questions that may have more than one answer. Checkboxes are a type of input.
  
  Rules are the same as for radio buttons.
  
  <label for="loving"><input id="loving" type="checkbox" name="personality"> Loving</label>
  
  When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type radio and checkbox report their values from the value attribute.
  
  <label for="indoor">
  <input id="indoor" value="indoor" type="radio" name="indoor-outdoor">Indoor
</label>
<label for="outdoor">
  <input id="outdoor" value="outdoor" type="radio" name="indoor-outdoor">Outdoor
</label>
  
  If you omit the value attribute, the submitted form data uses the default value, which is on. In this scenario, if the user clicked the "indoor" option and submitted the form, the resulting form data would be indoor-outdoor=on, which is not useful. So the value attribute needs to be set to something to identify the option.
  
  You can set a checkbox or radio button to be checked by default using the checked attribute.
  
  <input type="radio" name="test-name" checked>
  
  The div element, also known as a division element, is a general purpose container for other elements.

The div element is probably the most commonly used HTML element of all.
  
  At the top of your document, you need to tell the browser which version of HTML your page is using.  Most major browsers support the latest specification, which is HTML5. <!DOCTYPE html>.
  
  The ! and uppercase DOCTYPE is important, especially for older browsers. The html is not case sensitive.
  
  The rest of your HTML code needs to be wrapped in html tags
  
  <!DOCTYPE html>
<html>

</html>
  
  You can add another level of organization in your HTML document within the html tags with the head and body elements. Any markup with information about your page would go into the head tag. Then any markup with the content of the page (what displays for a user) would go into the body tag.

Metadata elements, such as link, meta, title, and style, typically go inside the head element.
  
  <!DOCTYPE html>
<html>
  <head>
    <meta />
  </head>
  <body>
    <div>
    </div>
  </body>
</html>
  
</details>

<details><summary>CSS</summary>
  
CSS, or Cascading Style Sheets, tell the browser how to display the text and other content that you write in HTML. With CSS, you can control the color, font, size, spacing, and many other aspects of HTML elements.
  
  We can do this by changing the style of your h2 element.
  
  color style property - change text color
  
  <h2 style="color: blue;">CatPhotoApp</h2>
  
  It is a good practice to end inline style declarations with a ; .
  
  <h2 style="color: red;">CatPhotoApp</h2> - styling that individual h2 element with inline CSS, which stands for Cascading Style Sheets.
  
  there's a better way to apply CSS. style block
  
  <style>
</style>
  
  Inside that style block, you can create a CSS selector for all h2 elements adding style definition with style rules.
  
  <style>
  h2 {
    color: red;
  }
</style>
  
  Classes are reusable styles that can be added to HTML elements.
  
  <style>
  .blue-text {
    color: blue;
  }
</style>
  
  You can apply a class to an HTML element like this: <h2 class="blue-text">CatPhotoApp</h2>.
  In your HTML elements' class attribute, the class name does not include the period.
  Classes allow you to use the same CSS styles on multiple HTML elements.
  
  
  Font size is controlled by the font-size CSS property, like this:
  
  h1 {
  font-size: 30px;
}
  
  You can set which font an element should use, by using the font-family property.
  
  h2 {
  font-family: sans-serif;
}
  
  In addition to specifying common fonts that are found on most operating systems, we can also specify non-standard, custom web fonts for use on our website.
  Google Fonts is a free library of web fonts that you can use in your CSS by referencing the font's URL.
  
  <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
  
  Now you can use the Lobster font in your CSS by using Lobster as the FAMILY_NAME as in the following example:
  
  font-family: FAMILY_NAME, GENERIC_NAME;
  
  The GENERIC_NAME is optional, and is a fallback font in case the other specified font is not available.
  
  Family names are case-sensitive and need to be wrapped in quotes if there is a space in the name. You need quotes to use the "Open Sans" font, but not to use the Lobster font.
  
  There are several default fonts that are available in all browsers. These generic font families include monospace, serif and sans-serif.
  
  When one font isn't available, you can tell the browser to "degrade" to another font.

  p {
  font-family: Helvetica, sans-serif;
}
  
  Generic font family names are not case-sensitive. Also, they do not need quotes because they are CSS keywords.
  
CSS has a property called width that controls an element's width. Just like with fonts, we'll use px (pixels) to specify the image's width.
  
  <style>
  .larger-image {
    width: 500px;
  }
</style>
  
  CSS borders have properties like style, color and width.
  
  <style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
  }
</style>
  
   you can apply multiple classes to an element using its class attribute, by separating each class name with a space. 
  
  <img class="class1 class2">
  
  We can round out those corners with a CSS property called border-radius. You can specify a border-radius with pixels.
  In addition to pixels, you can also specify the border-radius using a percentage.
  
  You can set an element's background color with the background-color property.
  
  .green-background {
  background-color: green;
}
  
  In addition to classes, each HTML element can also have an id attribute.
  
   You can use an id to style a single element and you can use them to select and modify specific elements with JavaScript.
  id attributes should be unique. Browsers won't enforce this, but it is a widely agreed upon best practice.
  
  <h2 id="cat-photo-app">
  
  id attributes is that, like classes, you can style them using CSS.

However, an id is not reusable and should only be applied to one element. An id also has a higher specificity (importance) than a class so if both are applied to the same element and have conflicting styles, the styles of the id will be applied.
  
  #cat-photo-element {
  background-color: green;
}
  
  Note that inside your style element, you always reference classes by putting a . in front of their names. You always reference ids by putting a # in front of their names.
  
    All HTML elements are essentially little rectangles. Three important properties control the space that surrounds each HTML element: padding, border, and margin. An element's padding controls the amount of space between the element's content and its border.
    
    An element's margin controls the amount of space between an element's border and surrounding elements. If you set an element's margin to a negative value, the element will grow larger.
     
    CSS allows you to control the padding of all four individual sides of an element with the padding-top, padding-right, padding-bottom, and padding-left properties.
    
    or padding: 10px 20px 10px 20px; - These four values work like a clock: top, right, bottom, left

CSS allows you to control the margin of all four individual sides of an element with the margin-top, margin-right, margin-bottom, and margin-left properties.
    
    or margin: 10px 20px 10px 20px; - These four values work like a clock: top, right, bottom, left
    
    
    You have been adding id or class attributes to elements that you wish to specifically style. These are known as ID and class selectors. There are other CSS Selectors you can use to select custom groups of elements to style.
    
  [attr=value] attribute selector to style the checkboxes - This selector matches and styles elements with a specific attribute value.
    
    [type='radio'] {
  margin: 20px 0px 20px 0px;
}
    
Pixels are a type of length unit, which is what tells the browser how to size or space an item. In addition to px, CSS has a number of different length unit options that you can use.    
    
The two main types of length units are absolute and relative. Absolute units tie to physical units of length. For example, in and mm refer to inches and millimeters, respectively. Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.    
    
 Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font. If you use it to set the font-size property itself, it's relative to the parent's font-size.   
    
There are several relative unit options that are tied to the size of the viewport.   
    
    Every HTML page has a body element.
    
    body {
  background-color: black;
}
    
    Remember, you can style your body element just like any other HTML element, and all your other elements will inherit your body element's styles.
    
    Sometimes your HTML elements will receive multiple styles that conflict with one another.
    
    We just proved that our classes will override the body element's CSS.
    
    
    Applying multiple class attributes to a HTML element is done with a space between them like this:

class="class1 class2"
Note: It doesn't matter which order the classes are listed in the HTML element.
    
   However, the order of the class declarations in the <style> section is what is important. The second declaration will always take precedence over the first. 
    
    We just proved that browsers read CSS from top to bottom in order of their declaration. That means that, in the event of a conflict, the browser will use whichever CSS declaration came last.
    
    Note: It doesn't matter whether you declare this CSS above or below pink-text class, since the id attribute will always take precedence. So we've proven that id declarations override class declarations, regardless of where they are declared in your style element CSS.
    
    We just proved that inline styles will override all the CSS declarations in your style element.
    
 In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important.   
    
    color: red !important;
    
   We usually use decimals, or base 10 numbers, which use the symbols 0 to 9 for each digit. Hexadecimals (or hex) are base 16 numbers. This means it uses sixteen distinct symbols. Like decimals, the symbols 0-9 represent the values zero to nine. Then A,B,C,D,E,F represent the values ten to fifteen. Altogether, 0 to F can represent a digit in hexadecimal, giving us 16 total possible values. 
    
    In CSS, we can use 6 hexadecimal digits to represent colors, two each for the red (R), green (G), and blue (B) components. For example, #000000 is black and is also the lowest possible value.
    
    body {
  color: #000000;
}
    
    From these three pure colors (red, green, and blue), we can vary the amounts of each to create over 16 million other colors!
    
    The digit 0 is the lowest number in hex code, and represents a complete absence of color.

The digit F is the highest number in hex code, and represents the maximum possible brightness.
    
    
    Dodger Blue	#1E90FF
Green	#00FF00
Orange	#FFA500
Red	#FF0000
    
    Many people feel overwhelmed by the possibilities of more than 16 million colors. And it's difficult to remember hex code. Fortunately, you can shorten it.
    
    For example, red's hex code #FF0000 can be shortened to #F00. This shortened form gives one digit for red, one digit for green, and one digit for blue.

This reduces the total number of possible colors to around 4,000. But browsers will interpret #FF0000 and #F00 as exactly the same color.
    
    Another way you can represent colors in CSS is by using RGB values.
    
    Instead of using six hexadecimal digits like you do with hex code, with RGB you specify the brightness of each color with a number between 0 and 255.

If you do the math, the two digits for one color equal 16 times 16, which gives us 256 total values. So RGB, which starts counting from zero, has the exact same number of possible values as hex code.
    
    
    
    body {
  background-color: rgb(255, 165, 0);
}
    
    Just like with hex code, you can mix colors in RGB by using combinations of different values.
    
    CSS Variables are a powerful way to change many CSS style properties at once by changing only one value.
    --penguin-skin: black;
    background: var(--penguin-skin, gray);
    
    
    
    To create a CSS variable, you just need to give it a name with two hyphens in front of it and assign it a value like this:

--penguin-skin: gray;
This will create a variable named --penguin-skin and assign it the value of gray. Now you can use that variable elsewhere in your CSS to change the value of other properties to gray.
    
    After you create your variable, you can assign its value to other CSS properties by referencing the name you gave it.
    
    background: var(--penguin-skin);
    
    Note that styles will not be applied unless the variable names are an exact match.
    
    When using your variable as a CSS property value, you can attach a fallback value that your browser will revert to if the given variable is invalid.
    
    Note: This fallback is not used to increase browser compatibility, and it will not work on IE browsers. Rather, it is used so that the browser has a color to display if it cannot find your variable.
    
    background: var(--penguin-skin, black);
    
    This will set background to black if your variable wasn't set. Note that this can be useful for debugging.
    
    When working with CSS you will likely run into browser compatibility issues at some point. This is why it's important to provide browser fallbacks to avoid potential problems.

When your browser parses the CSS of a webpage, it ignores any properties that it doesn't recognize or support. For example, if you use a CSS variable to assign a background color on a site, Internet Explorer will ignore the background color because it does not support CSS variables. In that case, the browser will use whatever value it has for that property. If it can't find any other value set for that property, it will revert to the default value, which is typically not ideal.

This means that if you do want to provide a browser fallback, it's as easy as providing another more widely supported value immediately before your declaration. That way an older browser will have something to fall back on, while a newer browser will just interpret whatever declaration comes later in the cascade.
    
    When you create a variable, it is available for you to use inside the selector in which you create it. It also is available in any of that selector's descendants. This happens because CSS variables are inherited, just like ordinary properties.

To make use of inheritance, CSS variables are often defined in the :root element.

:root is a pseudo-class selector that matches the root element of the document, usually the html element. By creating your variables in :root, they will be available globally and can be accessed from any other selector in the style sheet.
    
    When you create your variables in :root they will set the value of that variable for the whole page.

You can then over-write these variables by setting them again within a specific selector.
    
    CSS Variables can simplify the way you use media queries.

For instance, when your screen is smaller or larger than your media query break point, you can change the value of a variable, and it will apply its style wherever it is used.
    
    Visual design is a combination of typography, color theory, graphics, animation, page layout, and more to help deliver your unique message.
    
text-align: justify; spaces the text so that each line has equal width.

text-align: center; centers the text

text-align: right; right-aligns the text

And text-align: left; (the default) left-aligns the text.

You can specify the width of an element using the width property in CSS. Values can be given in relative length units (such as em), absolute length units (such as px), or as a percentage of its containing parent element.
    
    img {
  width: 220px;
}
    
    You can specify the height of an element using the height property in CSS, similar to the width property.
    
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
    
    Instead of adjusting your overall background or the color of the text to make the foreground easily readable, you can add a background-color to the element holding the text you want to emphasize. 
    
    rgba stands for:
  r = red
  g = green
  b = blue
  a = alpha/level of opacity
    
    The RGB values can range from 0 to 255. The alpha value can range from 1, which is fully opaque or a solid color, to 0, which is fully transparent or clear. rgba() is great to use in this case, as it allows you to adjust the opacity. This means you don't have to completely block out the background.
    
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
    
    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
    
 The opacity property in CSS is used to adjust the opacity, or conversely, the transparency for an item.   
    A value of 1 is opaque, which isn't transparent at all.
A value of 0.5 is half see-through.
A value of 0 is completely transparent.
The value given will apply to the entire element, whether that's an image with some transparency, or the foreground and background colors for a block of text.
    
   The text-transform property in CSS is used to change the appearance of text. It's a convenient way to make sure text on a webpage appears consistently, without having to change the text content of the actual HTML elements.
    
    lowercase	"transform me"
uppercase	"TRANSFORM ME"
capitalize	"Transform Me"
initial	Use the default value
inherit	Use the text-transform value from the parent element
none	Default: Use the original text
    
 The font-size property is used to specify how large the text is in a given element. This rule can be used for multiple elements to create visual consistency of text on a page   
    
    The font-weight property sets how thick or thin characters are in a section of text.

The font-size property in CSS is not limited to headings, it can be applied to any element containing text.
    
    CSS offers the line-height property to change the height of each line in a block of text. As the name suggests, it changes the amount of vertical space that each line of text gets.
    
     A pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.

For example, the styling of an anchor tag can be changed for its hover state using the :hover pseudo-class selector.
    
    a:hover {
  color: red;
}
    
    CSS treats each HTML element as its own box, which is usually referred to as the CSS Box Model. Block-level items automatically start on a new line (think headings, paragraphs, and divs) while inline items sit within surrounding content (like images or spans). The default layout of elements in this way is called the normal flow of a document, but CSS offers the position property to override it.

When the position of an element is set to relative, it allows you to specify how CSS should move it relative to its current position in the normal flow of the page. It pairs with the CSS offset properties of left or right, and top or bottom. These say how many pixels, percentages, or ems to move the item away from where it is normally positioned.
    
    p {
  position: relative;
  bottom: 10px;
}
    
    Changing an element's position to relative does not remove it from the normal flow - other elements around it still behave as if that item were in its default position.

Note: Positioning gives you a lot of flexibility and power over the visual layout of a page. It's good to remember that no matter the position of elements, the underlying HTML markup should be organized and make sense when read from top to bottom. This is how users with visual impairments (who rely on assistive devices like screen readers) access your content.
    
    The CSS offsets of top or bottom, and left or right tell the browser how far to offset an item relative to where it would sit in the normal flow of the document. You're offsetting an element away from a given spot, which moves the element away from the referenced side (effectively, the opposite direction).
    
    The next option for the CSS position property is absolute, which locks the element in place relative to its parent container. Unlike the relative position, this removes the element from the normal flow of the document, so surrounding items ignore it. The CSS offset properties (top or bottom and left or right) are used to adjust the position.

One nuance with absolute positioning is that it will be locked relative to its closest positioned ancestor. If you forget to add a position rule to the parent item, (this is typically done using position: relative;), the browser will keep looking up the chain and ultimately default to the body tag.
    
    
    The next layout scheme that CSS offers is the fixed position, which is a type of absolute positioning that locks an element relative to the browser window. Similar to absolute positioning, it's used with the CSS offset properties and also removes the element from the normal flow of the document. Other items no longer "realize" where it is positioned, which may require some layout adjustments elsewhere.

One key difference between the fixed and absolute positions is that an element with a fixed position won't move when the user scrolls.
    
    The next positioning tool does not actually use position, but sets the float property of an element. Floating elements are removed from the normal flow of a document and pushed to either the left or right of their containing parent element. It's commonly used with the width property to specify how much horizontal space the floated element requires.
    
    When elements are positioned to overlap (i.e. using position: absolute | relative | fixed | sticky), the element coming later in the HTML markup will, by default, appear on the top of the other elements. However, the z-index property can specify the order of how elements are stacked on top of one another. It must be an integer (i.e. a whole number and not a decimal), and higher values for the z-index property of an element move it higher in the stack than those with lower values.
    
    Another positioning technique is to center a block element horizontally. One way to do this is to set its margin to a value of auto.

This method works for images, too. Images are inline elements by default, but can be changed to block elements when you set the display property to block.
    
    Color theory and its impact on design is a deep topic and only the basics are covered in the following challenges. On a website, color can draw attention to content, evoke emotions, or create visual harmony. Using different combinations of colors can really change the look of a website, and a lot of thought can go into picking a color palette that works with your content.

The color wheel is a useful tool to visualize how colors relate to each other - it's a circle where similar hues are neighbors and different hues are farther apart. When two colors are opposite each other on the wheel, they are called complementary colors. They have the characteristic that if they are combined, they "cancel" each other out and create a gray color. However, when placed side-by-side, these colors appear more vibrant and produce a strong visual contrast.
    
   This is different than the outdated RYB color model that many of us were taught in school, which has different primary and complementary colors. Modern color theory uses the additive RGB model (like on a computer screen) and the subtractive CMY(K) model (like in printing). 
    
   Note: Using color can be a powerful way to add visual interest to a page. However, color alone should not be used as the only way to convey important information because users with visual impairments may not understand that content. 
    
 Computer monitors and device screens create different colors by combining amounts of red, green, and blue light. This is known as the RGB additive color model in modern color theory. Red (R), green (G), and blue (B) are called primary colors. Mixing two primary colors creates the secondary colors cyan (G + B), magenta (R + B) and yellow (R + G).   
    
    These secondary colors happen to be the complement to the primary color not used in their creation, and are opposite to that primary color on the color wheel. For example, magenta is made with red and blue, and is the complement to green.

Tertiary colors are the result of combining a primary color with one of its secondary color neighbors. For example, within the RGB color model, red (primary) and yellow (secondary) make orange (tertiary). This adds six more colors to a simple color wheel for a total of twelve.

There are various methods of selecting different colors that result in a harmonious combination in design. One example that can use tertiary colors is called the split-complementary color scheme. This scheme starts with a base color, then pairs it with the two colors that are adjacent to its complement. The three colors provide strong visual contrast in a design, but are more subtle than using two complementary colors.
    
    opposite colors on the color wheel can make each other appear more vibrant when placed side-by-side. However, the strong visual contrast can be jarring if it's overused on a website, and can sometimes make text harder to read if it's placed on a complementary-colored background. In practice, one of the colors is usually dominant and the complement is used to bring visual attention to certain content on the page.
    
    
   Colors have several characteristics including hue, saturation, and lightness. CSS3 introduced the hsl() function as an alternative way to pick a color by directly stating these characteristics.

Hue is what people generally think of as 'color'. If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line. In hsl(), hue uses a color wheel concept instead of the spectrum, where the angle of the color on the circle is given as a value between 0 and 360.

Saturation is the amount of gray in a color. A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray. This is given as a percentage with 100% being fully saturated.

Lightness is the amount of white or black in a color. A percentage is given ranging from 0% (black) to 100% (white), where 50% is the normal color. 
    
   The hsl() option in CSS also makes it easy to adjust the tone of a color. Mixing white with a pure hue creates a tint of that color, and adding black will make a shade. Alternatively, a tone is produced by adding gray or by both tinting and shading. Recall that the 's' and 'l' of hsl() stand for saturation and lightness, respectively. The saturation percent changes the amount of gray and the lightness percent determines how much white or black is in the color. This is useful when you have a base hue you like, but need different variations of it. 
    
    Applying a color on HTML elements is not limited to one flat hue. CSS provides the ability to use color transitions, otherwise known as gradients, on elements. This is accessed through the background property's linear-gradient() function.
    
    background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);

    The first argument specifies the direction from which color transition starts - it can be stated as a degree, where 90deg makes a horizontal gradient (from left to right) and 45deg makes a diagonal gradient (from bottom left to top right). The following arguments specify the order of colors used in the gradient.
    
    background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
    
   The repeating-linear-gradient() function is very similar to linear-gradient() with the major difference that it repeats the specified gradient pattern. repeating-linear-gradient() accepts a variety of values.
    
    The angle value is the direction of the gradient. Color stops are like width values that mark where a transition takes place, and are given with a percentage or a number of pixels.
    
    repeating-linear-gradient(
      90deg,
      yellow 0px,
      blue 40px,
      green 40px,
      red 80px
    );
    
     It helps to think about the color stops as pairs where every two colors blend together.
    
    0px [yellow -- blend -- blue] 40px [green -- blend -- red] 80px
    
    If every two color stop values are the same color, the blending isn't noticeable because it's between the same color, followed by a hard transition to the next color, so you end up with stripes.
    
    One way to add texture and interest to a background and have it stand out more is to add a subtle pattern. The key is balance, as you don't want the background to stand out too much, and take away from the foreground. The background property supports the url() function in order to link to an image of the chosen texture or pattern. The link address is wrapped in quotes inside the parentheses.
    
    To change the scale of an element, CSS has the transform property, along with its scale() function. 
    
    p {
  transform: scale(2);
}
    
    The transform property has a variety of functions that let you scale, move, rotate, skew, etc., your elements. When used with pseudo-classes such as :hover that specify a certain state of an element, the transform property can easily add interactivity to your elements.
    
    p:hover {
  transform: scale(2.1);
}
    
    Note: Applying a transform to a div element will also affect any child elements contained in the div.
    
    The next function of the transform property is skewX(), which skews the selected element along its X (horizontal) axis by a given degree.
    
    p {
  transform: skewX(-32deg);
}
    
    The skewY() property skews an element along the Y (vertical) axis.
    
    
 By manipulating different selectors and properties, you can make interesting shapes.  
    
     The box-shadow property that sets the shadow of an element, along with the border-radius property that controls the roundness of the element's corners.
    
    In order to create a round object, the border-radius property should be set to a value of 50%.
    
    
    You may recall from an earlier challenge that the box-shadow property takes values for offset-x, offset-y, blur-radius, spread-radius and a color value in that order. The blur-radius and spread-radius values are optional.
    
    You need to understand the ::before and ::after pseudo-elements. ::before creates a pseudo-element that is the first child of the selected element; ::after creates a pseudo-element that is the last child of the selected element.
    
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
    
    For the ::before and ::after pseudo-elements to function properly, they must have a defined content property. This property is usually used to add things like a photo or text to the selected element. When the ::before and ::after pseudo-elements are used to make shapes, the content property is still required, but it's set to an empty string.
    
Use the rotate() function with -45 degrees.    
    
     The animation properties control how the animation should behave and the @keyframes rule controls what happens during that animation. There are eight animation properties in total.
    
    animation-name sets the name of the animation, which is later used by @keyframes to tell CSS which rules go with which animations.

animation-duration sets the length of time for the animation.

@keyframes is how to specify exactly what happens within the animation over the duration. This is done by giving CSS properties for specific "frames" during the animation, with percentages ranging from 0% to 100%.
    
    CSS applies the magic to transition the element over the given duration to act out the scene.
    
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
    
    
    You aren't limited to only beginning-end transitions, you can set properties for the element for any percentage between 0% and 100%.
    
    
    You can use CSS @keyframes to change the color of a button in its hover state.
    
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
    
   The animation-fill-mode specifies the style applied to an element when the animation has finished. 
    
    animation-fill-mode: forwards;
    
    
    When elements have a specified position, such as fixed or relative, the CSS offset properties right, left, top, and bottom can be used in animation rules to create movement.
    
    
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
    
   the opacity of an animated element so it gradually fades 
    
    Another animation property is the animation-iteration-count, which allows you to control how many times you would like to loop through the animation.
    
    animation-iteration-count: 3;
    
    it's possible to make the animation run continuously by setting that value to infinite.
    
    You can change the @keyframes rule for one of the elements so the stars twinkle at different rates.
    
  @keyframes twinkle-1 {
    20% {
      transform: scale(0.5);
      opacity: 0.5;
    }
  }

  @keyframes twinkle-2 {
    50% {
      transform: scale(0.5);
      opacity: 0.5;
    }
  }   
    
    
    You can achieve the same goal by manipulating the animation-duration of multiple elements.
    
    To make them twinkle at different rates, you can set the animation-duration property to different values for each element.
    
    In CSS animations, the animation-timing-function property controls how quickly an animated element changes over the duration of the animation.
    
    There are a number of predefined keywords available for popular options. For example, the default value is ease, which starts slow, speeds up in the middle, and then slows down again in the end. Other options include ease-out, which is quick in the beginning then slows down, ease-in, which is slow in the beginning, then speeds up at the end, or linear, which applies a constant animation speed throughout.
    
    CSS offers an option other than keywords that provides even finer control over how the animation plays out, through the use of Bezier curves.

In CSS animations, Bezier curves are used with the cubic-bezier function. The shape of the curve represents how the animation plays out. The curve lives on a 1 by 1 coordinate system. The X-axis of this coordinate system is the duration of the animation (think of it as a time scale), and the Y-axis is the change in the animation.

The cubic-bezier function consists of four main points that sit on this 1 by 1 grid: p0, p1, p2, and p3. p0 and p3 are set for you - they are the beginning and end points which are always located respectively at the origin (0, 0) and (1, 1). You set the x and y values for the other two points, and where you place them in the grid dictates the shape of the curve for the animation to follow. This is done in CSS by declaring the x and y values of the p1 and p2 "anchor" points in the form: (x1, y1, x2, y2). 
    
    animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);
    
    In general, changing the p1 and p2 anchor points drives the creation of different Bezier curves, which controls how the animation progresses through time. 
    
    animation-timing-function: cubic-bezier(0, 0, 0.58, 1);
    
    Remember that all cubic-bezier functions start with p0 at (0, 0) and end with p3 at (1, 1).
    
    The animation-timing-function automatically loops at every keyframe when the animation-iteration-count is set to infinite. Since there is a keyframe rule set in the middle of the animation duration (at 50%), it results in two identical animation progressions at the upward and downward movement of the ball.
    
    
    The following cubic Bezier curve simulates a juggling movement:

cubic-bezier(0.3, 0.4, 0.5, 1.6);
    
    Although the cubic Bezier curve is mapped on a 1 by 1 coordinate system, and it can only accept x values from 0 to 1, the y value can be set to numbers larger than one. This results in a bouncing movement that is ideal for simulating the juggling ball.
    
    
   In web development, accessibility refers to web content and a UI (user interface) that can be understood, navigated, and interacted with by a broad audience. This includes people with visual, auditory, mobility, or cognitive disabilities. 
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
</details>

<details><summary>JavaScript</summary>
  

  
</details>


