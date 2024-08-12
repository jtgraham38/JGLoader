# JGLoader
jg_loader.js is a simple script containing a single function: *jg_get_loader*.  This function creates a loader element, and returns the object, where it can then be used however the programmer desires within the javascript.
```html
<button onclick="async_task(event)">Show Modal</button>

<div id="loader_container"></div>

<script>
async function async_task(event){

    let container = document.getElementById('loader_container')
    let loader = jg_get_loader()
    container.innerHTML = ""
    container.appendChild(loader)

    //execute some async task here...

    container.innerHTML = ""

    //do something with the result
}
</script>
```

There is a default loader for when no custom content is defined.  To customize the content of the loader, define a template in the body of your document with an id of *jg_loader_content*.

```html
<template id="jg_loader_content">
    <i class="fa-solid fa-xl fa-gear fa-spin"></i>
</template>
```

To style the loader content, target the *jg_loader* class.
