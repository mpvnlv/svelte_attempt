<script lang="ts">
    
</script>
<main>
    <div class = "cats">
        <img class = "cat" alt="First funny cat" src = "./build/wow-interesting.gif">
        <img class = "cat2" alt="Another funny cat" src = "./build/happy-smile.gif">
    </div>

</main>

<style>
@media (min-width:500px) {
  .cat{
    margin-top: 5%;
    margin-right: 10%;
    width: 28.645%;
    box-sizing: border-box;
    display: inline-block;
    border-radius: 20px;
    border: outset #04346C 1em ;
  }
  .cat2{
    margin-top: 5%;
    width: 30%;
    border-radius: 20px;
    box-sizing: border-box;
    border-radius: 20px;
    display: inline-block;
    border: outset #04346C 1em ;
  }
  .cats{
    height: 70%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
@media (max-width:500px) {
  .cat{
    margin-top: 5%;
   
    width: 70%;
    box-sizing: border-box;
    display: block;
    border-radius: 20px;
    border: outset #04346C 1em ;
  }
  .cat2{
    margin-top: 3%;
    width: 70%;
    display: block;
    box-sizing: border-box;
    border-radius: 20px;
    display: inline-block;
    border: outset #04346C 1em ;
  }
  
}

</style>