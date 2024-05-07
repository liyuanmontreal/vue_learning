<template>
  <h1>Teleport</h1>
  <p>Teleport is a built-in component that allows us to "teleport" a part of a component's template into a DOM node that exists outside the DOM hierarchy of that component.</p>
  <p>With &lt;teleport to="body"&gt; we move the red &lt;div&gt; from inside the component to the body tag.</p>
  <comp-one></comp-one>

    <div id="modal1">div in parent page </div>


  <div>   
    <teleport to="#modal1">
      <div class="yellowDiv">This modal is teleported to target from parent page.</div>
    </teleport>

    <teleport to="#div4">
      <div id="redDiv">Hello! I will show in the div 4 </div>
    </teleport>
    <teleport to="#modal2">
      <div class="yellowDiv">This modal is teleported to target  from parent page.</div>
    </teleport>

  </div>

</template>

<script></script>

<style>
  #app {
    width: 350px;
    margin: 10px;
  }
  #app > div {
    border: solid black 2px;
    padding: 10px;
    margin-top: 10px;
    background-color: rgb(186, 228, 255);
  }
  h2 {
    text-decoration: underline;
  }

  #redDiv {
    background-color: lightcoral;
    margin: 10px;
    padding: 10px;
    display: inline-block;
  }
  .yellowDiv {
    background-color: yellow;
    margin: 10px;
    padding: 10px;
    display: inline-block;
  }
</style>     