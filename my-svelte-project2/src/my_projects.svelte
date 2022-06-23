<script lang="ts">
 async function fetchbad(){
    const res = await fetch("https://api.imgflip.com/get_memes");
    const json = await res.json();
    console.log(json.data.memes[0].name);
    console.log(json.data)
    return json;
}


let name:string;
let src_photo:string;
fetchbad().then(memes =>{
    console.log(memes.data.memes[0].name);
    const mem_photo = new Image();
    let k:number = 0;

  
    name = memes.data.memes[k].name;
    src_photo = memes.data.memes[k].url;
    mem_photo.style.width = "100%";
    mem_photo.style.margin = "auto"
    
    
    const variable2 =  document.querySelector("#btn_mem") as HTMLButtonElement;
    let variable: HTMLButtonElement;
    

    if (variable2){
        variable = variable2;
        variable.onclick = function(){
            k=k+1;
            name = memes.data.memes[k].name;
            src_photo = memes.data.memes[k].url;
            mem_photo.style.width = "100%";
            mem_photo.style.margin = "auto"
            
            if (k===100){
              k = 0;
            }
          
    }
}


    })
</script>
<main>
  <div class = "try">
    <p id = "memes">{name}</p>
    <img id = "memes_photo" src ="{src_photo}" alt = "memes">
    <button id = "btn_mem">Generate MEMES</button>
</div>

</main>


<style>

  
  img{
    width: 100%;
  }
    .try{
  display: flex;
  flex-direction: column;
}
#memes{
  font-size:xx-large;
  font-family: "Mistral";
  align-self: center;


}
@media (min-width:499px){
  #memes_photo{
    align-self: center;
    box-sizing:border-box;
    width: 20%;
    height: 40vh; 
  }
}
@media (max-width:500px) {
  #memes_photo{
    align-self: center;
    box-sizing:border-box;
    width: 50%;
    height: 25vh; 
  }
}
#btn_mem{
  display: flex;
  color: black;
  justify-content:center ;
  font-weight: bold;
  align-self: center;
  margin-top: 10%;
  height: 5vh;
  width: 30vh;
  border-radius: 20px;
  background-color: #3F92D2;
  border: ridge 0.5vh #04346C;
}

</style>