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
    
    
    
    
    
    
    
    
    
</details>

<details><summary>JavaScript</summary>

</details>


