<script lang="ts">
	
</script>


	<div id="navbar">
		<div on:click={()=>{location.href='../../my-svelte-project2/public/index.html'}} class = "menu2"><span href = "">My projects</span></div>
		<div on:click={()=>{location.href='../../my-svelte-project/public/index.html' }}  class = "menu2"><span>Funny Cats</span></div>
		<div on:click={()=>{location.href='../../my-svelte-project4/public/index.html' }} class = "menu"><span href = "">Main page</span></div>
    <div on:click={()=>{location.href='../../my-svelte-project3/public/index.html' }} class = "menu"><span href = "">About me</span></div>
	</div>


<style>
	#navbar {
  margin: 0;
  padding: 0;
  list-style-type: none;
  width: 100%;
  margin-top: 2%;
  display: flex;
  justify-content: center;
  }
 span{
    color: aliceblue;
    text-decoration:none;
    line-height:2em ;
    font-size: 100%;
  }
  @media (max-width: 500px){
    .menu, .menu2{
      width: 50%;
      border: ridge 0.5vh #04346C;
  
      text-align: center;
      border-radius: 20px;
      display: inline-block;
      margin: 0.5%;
      background-color: #04346C;
    }
  }
  @media (min-width:500px) {
    .menu, .menu2{
      width: 15%;
      border: ridge 0.5vh #04346C;
  
      text-align: center;
      border-radius: 20px;
      display: inline-block;
      margin: 0.5%;
      background-color: #04346C;
    }
  }
  .menu:hover{
    background-color: gray;
    opacity: 0.3;
    cursor: pointer;
  }

  .menu2:hover{
    background-color: gray;
    opacity: 0.3;
    cursor: pointer;
  }
 
</style>