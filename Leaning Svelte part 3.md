#Input Data Binding



As you now, Svelte is a “radical new approach to building user interfaces”, according to the official documentation. In practice, Svelte is quite similar to JavaScript frameworks like React, Vue etc.

Today i will write about Input data binding.

Inpunt bindings are essentially just a way you can keep variables inside your components in sync with input fields.

They are very handy when design forms  or having any form of data entry.

**bind:property**

Let’s start with the most common form of binding you’ll often use, which you can apply using bind:value. You take a variable from the component state, and you bind it to a form field:

 ```
 <script>
 
 Let name = “Alessandro”
 
 </script>
 
 <p> Your name is: {name}
 
 <input bind:value = {name}
 
 ```
 
 Now if name changes the input field will update its value. And the opposite is true, as well: if the form is updated by the user, the name variable value changes.


We successfully binded name variable to the input field, when the user makes change to the input field it is going to update the data within your components, this is the most basic example .

bind:value works on all flavors of input fields (type="number", type="email" and so on), but it also works for other kind of fields, like **textarea** and **select** 

Let's see an example:


```
<script>
let coffeeOrigins = ["Ethiopia","Colombia","Sumatra","India","Nicaragua"];
let selected;
</script>

<main>

<p> Your have choose: {selected || 'nothing'}</p>

{#each coffeeOrigins as origin}

<label>
<input type="radio" bind:group={selected} value={origin}/>
{origin}
</label>
{/each}

</main>

<style>
</style>


