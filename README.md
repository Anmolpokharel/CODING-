# CODING-<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
 <meta name="viewport" content="width=device-width, initial-scale=1">
<title>Untitled Document</title> 
<script type="text/javascript" src="js/jquery-1.5.2.js"></script>
<script type="text/javascript" src="js/jquery-ui.js"></script>
<script type="text/javascript" src="js/main.js"></script>

<link href="css/main.css" rel="stylesheet" type="text/css" />
   
<script type="text/javascript">  
$(window).load(function(){
function collision($div1, $div2) {
var x1 = $div1.offset().left;
var y1 = $div1.offset().top;
var h1 = $div1.outerHeight(true);
var w1 = $div1.outerWidth(true);
var b1 = y1 + h1;
var r1 = x1 + w1;
var x2 = $div2.offset().left;
var y2 = $div2.offset().top;
var h2 = $div2.outerHeight(true);
var w2 = $div2.outerWidth(true);
var b2 = y2 + h2;
var r2 = x2 + w2;

if (b1 < y2 || y1 > b2 || r1 < x2 || x1 > r2)   return false ;
endgame();   return true;
}


window.setInterval(function() {
 $('.result').text(collision($('#croco1'), $('#div2')));
$('.result').text(collision($('#croco2'), $('#div2')));
$('.result').text(collision($('#croco3'), $('#div2'))); 
$('.result').text(collision($('#enm1'), $('#div2')));
$('.result').text(collision($('#enm13'), $('#div2')));  
$('.result').text(collision($('#enm14'), $('#div2')));  

$('.result').text(collision($('#enm2'), $('#div2')));  
$('.result').text(collision($('#enm3'), $('#div2')));  
$('.result').text(collision($('#enm4'), $('#div2')));  
$('.result').text(collision($('#enm5'), $('#div2')));  
$('.result').text(collision($('#enm6'), $('#div2')));  
$('.result').text(collision($('#enm7'), $('#div2')));  
$('.result').text(collision($('#enm8'), $('#div2')));  
$('.result').text(collision($('#enm10'), $('#div2')));  
$('.result').text(collision($('#enm11'), $('#div2')));  
$('.result').text(collision($('#enm12'), $('#div2')));  
  

}, 200); }); 






/*------Get Points--------*/





$(window).load(function(){
function getpointscoin($div1, $div2, coin1) {
var ci = coin1;
var x1 = $div1.offset().left;
var y1 = $div1.offset().top;
var h1 = $div1.outerHeight(true);
var w1 = $div1.outerWidth(true);
var b1 = y1 + h1;
var r1 = x1 + w1;
var x2 = $div2.offset().left;
var y2 = $div2.offset().top;
var h2 = $div2.outerHeight(true);
var w2 = $div2.outerWidth(true);
var b2 = y2 + h2;
var r2 = x2 + w2; 
if (b1 < y2 || y1 > b2 || r1 < x2 || x1 > r2)   return false ;
addpoint(ci);   return true;
}


window.setInterval(function() {
 $('.result').text(getpointscoin($('#coin1'), $('#div2'),'#coin1')); 
 $('.result').text(getpointscoin($('#coin2'), $('#div2'),'#coin2')); 
 $('.result').text(getpointscoin($('#coin3'), $('#div2'),'#coin3')); 
 $('.result').text(getpointscoin($('#coin4'), $('#div2'),'#coin4')); 
 $('.result').text(getpointscoin($('#coin5'), $('#div2'),'#coin5')); 
 $('.result').text(getpointscoin($('#coin6'), $('#div2'),'#coin6')); 
 $('.result').text(getpointscoin($('#coin7'), $('#div2'),'#coin7')); 
 $('.result').text(getpointscoin($('#coin8'), $('#div2'),'#coin8')); 
 $('.result').text(getpointscoin($('#coin9'), $('#div2'),'#coin9')); 

}, 200); }); 

 
</script>



 
</head>

<body onload="stage1moving();yourFunction();">

<div class="bluesky" id="skydiv"><div id="stage">
<div class="mudroadtexture"></div>
<div class="crocodial"  style=" left:2000px;"><div style="position:relative;"><div class="waterwarn200" id="croco1"></div>
</div></div>

<div class="mudroadtexture" style=" left:2200px; width:800px;"></div>

<div class="mudroadtexture" style=" left:3200px; width:300px;"></div>
<div class="crocodial"  style=" left:3000px;"><div style="position:relative;"><div class="waterwarn200" id="croco2"></div>
</div></div>

<!--Fire Box-->

<div style="position:absolute; z-index:111; left:1600px; bottom:70px;" ><div style=" position:relative;"><img src="images/fire.gif"/><div style="position:absolute; width:60px; left:20px; top:0px; height:100px;"  id="enm13"></div></div></div>

<div style="position:absolute; z-index:111; left:2350px; bottom:60px;" ><div style=" position:relative;"><img src="images/fire.gif"/><div style="position:absolute; width:60px; left:20px; top:0px; height:100px;"  id="enm14"></div></div></div>



<div class="bridgetexture" style=" left:3500px; width:1900px;"></div>
<div class="crocodial"  style=" left:5400px;"><div style="position:relative;"><div class="waterwarn200" id="croco3"></div>
</div></div>
<div class="mudroadtexture" style=" left:5600px; width:5000px;"></div>


<div class="enmybox">
<div style="position:relative; width:100%; overflow:visible;">  
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:1000px; bottom:-150px;"  id="enm2"    />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:6500px; bottom:-150px;" id="enm4"   />
<img src="images/enm_stage1/bird1.png" class="bird"     style="position:absolute; left:3500px; bottom:20px;" id="enm1" />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:8800px; bottom:70px;"  id="enm3"   />

<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:10000px; bottom:-150px;"  id="enm5"   />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:12000px; bottom:-150px;"  id="enm6"   />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:13500px; bottom:-150px;"  id="enm7"   />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:15000px; bottom:60px;"  id="enm8"   /></div>



<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:10100px; bottom:60px;"  id="enm9"   />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:12005px; bottom:-150px;"  id="enm10"   />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:13500px; bottom:-150px;"  id="enm11"   />
<img src="images/enm_stage1/bird1.png" class="bird"      style="position:absolute; left:16000px; bottom:94px;"  id="enm12"   />










<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:1400px; top:100px;" id="coin1" />
<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:1450px; top:90px;"  id="coin2"/>
<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:1500px; top:80px;"  id="coin3"/>

<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:2300px; top:0px;" id="coin4" />
<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:2350px; top:20px;"  id="coin5"/>
<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:2900px; top:30px;"  id="coin6"/>


<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:3900px; top:0px;" id="coin7" />
<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:4400px; top:35px;"  id="coin8"/>
<img src="images/coin/c1.png" class="runcoin" style="position:absolute; left:4450px; top:20px;"  id="coin9"/>



 







</div>
</div>
 

</div> 
 <img src="images/jump.png"  style="position:absolute; z-index:55555; right:11px;  bottom:12px;"  onclick="player();" />

<div class="grasstree">
<div style="position:relative;">
<div class="grass"></div>

</div>
</div>
<div class="grasstree">
<div style="position:relative;">
<div class="grass"></div> 


</div>
</div>

<div class="seenlayer"><div class="kutubminar"></div></div>

<div class="maintree">
<div style="position:relative;">
<div class="tree1"></div> 
<div class="tree1" style="left:1200px;"></div> 
<div class="tree1" style="left:1800px;"></div> 
<div class="tree1" style="left:2600px;"></div> 
<div class="tree1" style="left:2800px;"></div> 
<div class="tree1" style="left:7000px;"></div> 


<div class="tree2" style="left:1600px;"></div> 
<div class="tree2" style="left:3500px;"></div> 
<div class="tree2" style="left:4400px;"></div> 
<div class="tree2" style="left:520px;"></div> 
<div class="tree2" style="left:6800px;"></div> 



</div>
</div>


<div style="position:absolute;    bottom:80px; left:201px; z-index:10000" id="box">
<div style="position:relative;" id="div2">
<span  id="changer">

<img src="images/running/frame-1.png"  id="player2"  />
<img src="images/Jump/Jump-up.png"  id="jump"  style="display:none;" />

</span>
<img src="images/Jump/Jump-fall.png" style="display:none; position:absolute; bottom:0px; left:0px;" id="endgamer" /></div> 



</div>
</div>










<!--Game Over Box-->
 
<div style="width:100%; margin-top:10%; position:fixed; width:100%; left:0px; top:0px; z-index:99999999; display:none; " id="gaveoverbox">
<div style="width:300px;  margin:auto; background-color:#FFFF99; border:5px solid #CC0000; box-shadow:0px 0px 30px #000; border-radius:10px; padding:20px; text-align:center; ">

<h1 class="style1">Game Over</h1>
<div style="font-size:25px; font-weight:bold; margin-bottom:10px; margin-top:10px;" >Total Score <span id="showscor"></span></div>
<div style="margin-top:10px; font-size:13px;">Retry Please</div>


<form style="margin-top:20px;">
<input type="submit"  style="background-color:red; border-radius:10px; padding:10px; color:green; border:2px solid #000; font-size:18px; font-family:Verdana, Arial, Helvetica, sans-serif;" value="Re-Start Game"/>
</form>
</div>
</div>

<!--Game Over Box-->






<!--Music Player-->

<div style="display:none;">
<audio controls  autoplay loop="loop"> 
  <source src="music/stage1.mp3" type="audio/mpeg" >
Your browser does not support the audio element.
</audio>
</div>



<audio id="player" >
<source src="music/coin.mp3" type="audio/mpeg" >

</audio>
<!--Music Player-->





<!--Score Box-->

<div id="scoreb" style=" padding:10px; background-color:#CC0000; color:#FFFFFF; font-size:25px; font-weight:bold; position:fixed; right:10px; top:10px; border:5px #FFFFFF; border-radius:50px;" >Score : <span id="doughnuts">0</span></div>

<!--Score Box-->


</body>
</html>
