---
layout: page
title: About
permalink: /about/
logo: /images/reverie.png
---
<div class="dark-light">
    <div class="icon-dark">
        {{> icons/light}}
    </div>
    <div class="icon-light">
        {{> icons/dark}}
    </div>
</div>
# Michael Corry Otieno

I am an aspiring **Software Engineer**.

I studied Computer Science in Masinde Muliro University of Science and Technology.

This website is my portfolio website for blogging and to showcase my projects.

<script>
    /*
* Dark Light Version
*/
var html = document.querySelector('html'),
darkLight = document.querySelector('.dark-light')
darkLight.addEventListener('click', function(){
   if(html.getAttribute('data-theme') === 'light'){
       html.setAttribute('data-theme', 'dark')
       localStorage.setItem('selected-theme', 'dark');
   }else{
       html.setAttribute('data-theme', 'light')
       localStorage.setItem('selected-theme', 'light');
   }
   console.log(html.hasAttribute('data-theme'))
})
if(typeof(Storage) !== 'undefined') {
   if (localStorage.getItem('selected-theme') == 'light') {
       document.documentElement.setAttribute('data-theme', 'light');
   }
   else if (localStorage.getItem('selected-theme') == 'dark') {
       document.documentElement.setAttribute('data-theme', 'dark');
   }
}
</script>