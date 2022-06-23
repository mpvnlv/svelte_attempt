<script lang="ts">
// function([string1, string2],target id,[color1,color2])    
consoleText(['Hello World.', 'I am Vika Kruk', 'This site made with Love.'], 'text',['#04346C','#04346C','#04346C']);
let con:HTMLElement;
let target: HTMLElement;
function consoleText(words, id, colors) {
  if (colors === undefined) colors = ['#fff'];
  var visible:boolean = true;
 
  
  var letterCount:number = 1;
  var x: number = 1;
  var waiting = false;

  window.setInterval(function() {

    target.setAttribute('style', 'color:' + colors[0])

    if (letterCount === 0 && waiting === false) {
      waiting = true;
      target.innerHTML = words[0].substring(0, letterCount)
      window.setTimeout(function() {
        var usedColor = colors.shift();
        colors.push(usedColor);
        var usedWord = words.shift();
        words.push(usedWord);
        x = 1;
        target.setAttribute('style', 'color:' + colors[0])
        letterCount += x;
        waiting = false;
      }, 1000)
    } else if (letterCount === words[0].length + 1 && waiting === false) {
      waiting = true;
      window.setTimeout(function() {
        x = -1;
        letterCount += x;
        waiting = false;
      }, 1000)
    } else if (waiting === false) {
      target.innerHTML = words[0].substring(0, letterCount)
      letterCount += x;
    }
  }, 120)
  window.setInterval(function() {
    if (visible === true) {
      con.className = 'console-underscore hidden'
      visible = false;

    } else {
      con.className = 'console-underscore'

      visible = true;
    }
  }, 400)
}
</script>
<main>
    <div  class='console-container'>
        <span bind:this={target} id='text'></span>
        <div bind:this={con} class='console-underscore' id='console'>  &#95;</div>
    </div>
</main>

<style>

.console-container {
    background-color: #FFB540	;
  font-family:Khula;
  font-size:250%;
  text-align:center;
  height:20%  ;
  width:50%;
  display:block;
  position:absolute;
  color:white;
  top:0;
  bottom:0;
  left:0;
  right:0;
  margin:auto;
}
.console-underscore {
    background-color: #FFB540	;
   display:inline-block;
  position:relative;
  top:-0.14em;
  left:1%
}

</style>