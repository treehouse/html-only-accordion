# html-only-accordion

Accordions are all over the web and mobile apps. They are a great way to show and hide content based on user interaction and aren’t very hard to build but usually require a bit of HTML, CSS and JavaScript. Did you know you could build a simple accordion in just seconds with only HTML? Follow along as I explain how to set this up!

The HTML accordion requires only two HTML tags to get set up. `<details>` and `<summary>`. The basic code structure would look like this:
```
<details>
   <summary></summary>
<details>
```
The details HTML tag
The `<details>` tag acts as a wrapper for our accordion. All of the content for your accordion must go inside of the `<details>` tag.

The summary HTML tag
The `<summary>` tag is usually used for your title. Before the accordion is clicked, this is the content that is visible and will always remain visible.

Adding content to an accordion
To add content to the accordion when the user clicks it is pretty simple. Any content underneath the `<summary>` tags will be hidden by default. This content could be anything from some paragraph tags, an ordered list, images, links, you name it. Once the user clicks the accordion, this content will be visible.

Here is some basic content:
```
<details>
   <summary>
      <h1>Todo list:</h1>
   </summary>
   <p>Study</p>
   <p>Grocery Shop</p>
   <p>Clean The House</p>
</details>
```
Pretty cool, with just a few lines of markup, we built a functioning accordion! As you can see it’s not the best looking accordion out there. No worries though, we can style it pretty easily!

How to Style an HTML Accordion
Styling your accordion is very much up to you and how you’d like for it to look, but feel free to follow along as I give just a few basic stylings to the one we created above.
```
details {
    width: 250px;
    padding: 1rem;
    border-radius: 8px;
    background: white;
    box-shadow: 4px 4px 3px rgba(0,0,0,0.15);
}
```
To the details CSS rule, ive added a fixed width, some padding, a border-radius, background color, and some box-shadow. Next we can style up our `<summary>` tag.
```
summary {
    cursor: pointer;
}
summary h1 {
    display: inline;
    margin-left: 1rem;
    font-size: 1.25rem;
}
```
First thing you’ll notice is I gave our summary a cursor: pointer. This is just so the accordion appears that it can be clicked to the user.

I then give some basic stylings to the h1 element so that it can remain on the same line as our caret that comes with the accordion menu by default. Some margin and a larger font-size has been added as well.

Lastly, we can style the paragraph tags we added by writing the following:
```
details p {
    margin-left: 1.75rem;
    opacity: 0.7;
}
```
And that’s about it. We now have a much cooler looking accordion!