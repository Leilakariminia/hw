<!DOCTYPE html>
<html>
    <head>
        <title>
            Timer
        </title>
    </head>
    <body>
        <h1>
            Timer
        </h1>
        <p id="idk">
        </p>
        <script>
            var countdowndate=new Date("mar 19,2024 5:31:53").getTime();
            var x=setInterval(function(){
            var now=new Date().getTime();
            var distance=countdowndate-now;
            var day=Math.floor(distance/(1000*60*60*24));
            var hour=Math.floor((distance%(1000*60*60*24))/(1000*60*60));
            var minutes=Math.floor((distance%(1000*60*60))
            /(1000*60));
            var seconds=Math.floor((distance%(1000*60))/1000);
            document.getElementById("idk").innerHTML=day+":"+hour+":"+minutes+":"+seconds;
            if(distance<0){
            clearInterval(x);
            document.getElementById("idk").innerHTML="Stop";
            }
            },1000);
            </script>
    </body>
</html>
