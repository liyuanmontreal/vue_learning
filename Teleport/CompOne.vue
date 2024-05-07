<template>
  <div>
      <h2>Component without Teleport</h2>
      <p>This is the inside of the component.</p>        
        <div id="redDiv">Hello! I will stay in the component </div>          
  </div>

  <div>
      <h2>Component with Teleport</h2>
      <p>My content will show on the body.</p>
      <Teleport to="body">
        <div id="redDiv">Hello! I will show in the body </div>
      </Teleport>
  </div>


  <div>
    <h2>Component with Telepoort 3</h2>
    <p>content from component 3 will  show in the div 4.</p>
    <Teleport to="#div4">
      <div id="blueDiv">Hello! I will show in the div 4 </div>
    </Teleport> 
</div>

<div id="div4">
  <h2>Component with Telepoort 4</h2>
  <p>content will show here</p>
</div>

 
<div id="modal2">div in child component </div>


    <teleport to="#modal1">
      <div class="blueDiv">This modal is teleported to target from component.</div>
    </teleport> 

    <teleport to="#modal2">
      <div class="blueDiv">This modal is teleported to target from component</div>
    </teleport> 


      
</template>

<script>

</script>

<style scoped>
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
  .blueDiv {
    background-color: blue;
    margin: 10px;
    padding: 10px;
    display: inline-block;
  }
</style>                  