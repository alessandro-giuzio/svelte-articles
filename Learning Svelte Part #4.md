# Learning Svelte Part #4

## Props and Components

Hello developers, welcome back to my series of articles about my journey to learn Svelte, this is my 4th post about it, and so far it’s very helpful for my learning, writing down my steps make it public make a good contribution to my knowledge.

Today I am writing about Props and Components.

Normally, a Svelte website is made with of many different components: App.svelte, Header.svelte, Content.svelte, Footer.svelte and so on. 
All this components will be structured to make up the full page, the root component it’s the App.svelte, this component will be directly deployed in the  Dom by the main.JS file.

We will nest all the others components with it.

![Svelte components structure](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ikujhpxpf5hked6f6dnm.png)

The question is: why we need to split our webapp in so many different pieces and not write all the code in the App.svelte root component?
The main reason is to keep your code easy to read, tidy and modular. Imagine we put everything in one module, the chances that our code will be disorganized are very high.
Another reason to split in different modules is that with this method we can easily reuse it, we can create components to use whenever we need.

We can easily import our components in the App.svelte  using the syntax import

![Script hero](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5je3lsnog2qy3xmc0cmf.png)

And then we will display it in our  HTML like in the follow example:

![hero](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qyzubw0y8283hlo6bq6n.png)

If we want to change any data in the reused component, we can do that, using props.

How can we pass props to a component?

We need to declare the props we want to pass in, in the component itself, we can call it how we like it and we need to set it to a value that ca be: a string, an object, could be an integer. When the components it’s created it will read the props and the value

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/u5mxcy99yy3w8iu77c2r.png)

To access the prop inside the Footer component we need to declare that we are going to use that variable called “prop” (you can name it how you like most) 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jsbtde7r3rf66x2xwp4y.png)

We declare the variable “prop”,  and set to “export” , so now this way we can access the value outside the component.

That’s it for my contribution today, it’s difficult for me write in English but I will keep going, please feel free to leave a comment and roast my explanation.


