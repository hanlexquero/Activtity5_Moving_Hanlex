<style type="text/css">
    img{
        width: 150px;
        height: 150px;
    }
    #hanlex{
        border-style: solid;
        border-color: black;
        width: 1335px;
        height: 600px;
        background-size: 100% 100%;

    }
</style>
<script lang="javascript">
    function move_pic(e)
    {
        document.getElementById('button1').style.backgroundColor="white";
        document.getElementById('button2').style.backgroundColor="white";
        document.getElementById('button3').style.backgroundColor="white";
        document.getElementById('button4').style.backgroundColor="white";

        d=e.keyCode;
        //alert(d);
        if(d=='39'){
        document.getElementById('box').innerHTML="<img src=IMG_3201.jpg />";
        pos=document.getElementById('box').style.left;
        pos=pos.substring(0, pos.length-2);
        pos=parseInt(pos)+100
        if(pos<=1199){
            document.getElementById('box').style.left=pos+"px";
        }
        else{
            document.getElementById('box').style.left=1199;
        }
        document.getElementById('button1').style.backgroundColor="pink";
        }

        if(d=='37'){
        document.getElementById('box').innerHTML="<img src=right1.jpg />";
        pos=document.getElementById('box').style.left;
        pos=pos.substring(0, pos.length-2);
        pos=parseInt(pos)-100;
        if(pos>=10){
            document.getElementById('box').style.left=pos+"px";
        }
        else{
            document.getElementById('box').style.left=10;
        }
        document.getElementById('button2').style.backgroundColor="gray";
        }

        if(d=='38'){
        document.getElementById('box').innerHTML="<img src=IMG_3139.jpg />";
        pos=document.getElementById('box').style.top;
        pos=pos.substring(0, pos.length-2);
        pos=parseInt(pos)-100;
        if(pos>=28){
            document.getElementById('box').style.top=pos+"px";
        }
        else{
            document.getElementById('box').style.top=28;
        }
        document.getElementById('button3').style.backgroundColor="red";
        }

        if(d=='40'){
        document.getElementById('box').innerHTML="<img src=up.jpg />";
        pos=document.getElementById('box').style.top;
        pos=pos.substring(0, pos.length-2);
        pos=parseInt(pos)+100;
        if(pos<=485){
            document.getElementById('box').style.top=pos+"px";
        }
        else{
            document.getElementById('box').style.top=485;
        }
        document.getElementById('button4').style.backgroundColor="blue";
        }
    }
</script>

<body onkeyup=move_pic(event);

<div id="b">
<input id=button1 type="button" value="Right" 
    onclick=move_pic(right) />  
<input id=button2 type="button" value="Left"
    onclick=move_pic(left) />  
<input id=button3 type="button" value="Up"
    onclick=move_pic(up) /> 
<input id=button4 type="button" value="Down"
    onclick=move_pic(down) />
    <div id="hanlex" value="border">
        <div id="box" style="top:300px; left:600px; position: absolute;">
        <img src="bigboy.jpg" />
        </div>
  </div>
</body>
