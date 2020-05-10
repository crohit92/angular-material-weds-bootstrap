<h1 align="center">Angular Material weds Bootstrap</h1>

<article align="center">
   <img src="./assets/angular-weds-bootstrap.png" alt="logo">
</article>

# You might have been using bootstrap the WRONG WAY !
**This post is for all Angular devs who `care for every byte downloaded` from the server to the client machine**

<p style="display:flex;align-items:flex-start;">
   <img src="./assets/avatar.png"> 
   <span style="padding-left:16px; display:flex;flex-direction:column; justify-content:space-between;">Hi, I am Rohit Chopra, an angular developer with strong focus on <b>application performance and maintainability.</b>
   <br/>
   <span>I am always willing to have a healthy debate about technology. So drop me a mail at <a href="mailto:crohit92@gmail.com">crohit92@gmail.com</a> anytime to start a discussion. 
   </span>
   </span>
</p>


I have been using angular along with angular material since 2015 because of the obvious reason that angular material is written in angular and it feels like a part of the framework. I don't feel that i am working on two different technologies, it's rather only angular with some prebuilt components available out of the box.

## Motivation for this post

Angular material is a great library but it is limited only to a set of components. There is no doubt that those components are written with great thought and they are highly flexible. They provide functionality which is neither less nor more than the intended.

But every frontend developer knows that there is much more required than just a toolkit of reusable components. 

We need: 
- Reusable CSS classes to size elements
- Reusable CSS classes to position elements on screen
- Reusable CSS utility classes for various properties like
   - display
   - visibility
   - position
   - padding
   - margin
   - width
   - and many more...
- A grid framework which is intutive and easy to understand and at the same time very robust.
- Rresponsive CSS utilities to adapts to the device width.

**All the above requirements point to one of the most famous design libraries i.e. `Bootstrap`**  

## The Necessary Evil - `Bootstrap`

Due to the requirements mentioned above, frontend devs generally end up using bootstrap in their project along with other design libraries(for components), like Angular Material in my case.

But why am i calling bootstrap an `Evil`? 

What is wrong in having two libraries when one just provides components and the other provide layout. They must be a perfect mix right ?

## Consequence of having bootstrap with Angular Material

There are some issues, I want to point out, which occur when we use both these design libraries together.

- The download bundle size increases more than the required
   - Because bootstrap does not by default allow you to pick and choose what features you want from it. You have to take everything as a single bundle.
- Bootstrap uses `!important` for almost every css utility which i hate the most. I always use the [Specificity rule](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) to override my styles when required. Using !important is a bad way of writing and should be avoided always.
- Extra scripting library `jquery` which is not recommended with Angular.
- Even extra JS for bootstrap as well - `bootstrap.js`

The above consequences should be enough to start thinking of a better solution.

