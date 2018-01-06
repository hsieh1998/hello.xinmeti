<html>
<link type="text/css" rel="stylesheet" href="home.css">
<head>
    <title>homepage</title>
    <meta http-equiv="content-type" content="text/html; charset=utf-8" />
        <script type="text/javascript">
window.onload=function(){
    
    var num=1;
    var tNum=4;
    var duration=4000;
    
    run();
    document.getElementById("box").onmouseover=stopRun;
    document.getElementById("box").onmouseout=run;
    
    for(var i=1; i<=tNum; i++){
        document.getElementById("tab"+i).onclick=show;
        document.getElementById("con"+i).style.display="none";
    }
    document.getElementById("con1").style.display="block";
    document.getElementById("tab1").className="now-tab";

//===========================================
    function autoShow(){
        for(var i=1; i<=tNum; i++){
            document.getElementById("con"+i).style.display="none";
            document.getElementById("tab"+i).className="";
        }
        if(num<tNum){ num++;}else{ num=1;}
        document.getElementById("con"+num).style.display="block";
        document.getElementById("tab"+num).className="now-tab";
    }
    
    function show(){
        num=this.id.substr(3)-1;
        autoShow();
    }
    
    function stopRun(){ clearInterval(myInterval);}
    
    function run(){ myInterval= setInterval( autoShow, duration);}
    
}
        </script>
</head>

<body>
    <div id="back">
        <div id="top">
            <img src="logo.png" width="20%" height="100%" >
            <div class="us" style="float:right; margin-right:10%; margin-top:0.5%;">
            <h2 >About Us</h2><p>這是一個由學生自製的網站 關注台灣的剩食問題 歡迎加入我們</p>
            </div>
        </div>        
        <div id="header" >
            <a href="https://dennishsiao.github.io/project/home.html"> 
                <img src="home1.png"  width="20%" height="80%" style="position:relative; top:10%; left:1%">
            </a>
            <a href="https://dennishsiao.github.io/project/game.html"> 
                <img src="game.png"  width="20%" height="80%" style="position:relative; top:10%; left:6.5%">
            </a>
            <a href="https://dennishsiao.github.io/project/video.html"> 
                <img src="video.png" width="20%" height="80%" style="position:relative; top:10%; left:12%">
            </a>
            <a href="https://dennishsiao.github.io/project/test.html"> 
                <img src="test.png"  width="20%" height="80%" style="position:relative; top:10%; left:17.5%">
            </a>
        </div>
        <div id=second>
            <div class="tabPanel" id="box">
                <div class="tab-content" id="con1">
                    <img src="001.jpg" width="100%" height="100%" >
                </div>
                <div class="tab-content" id="con2">
                    <img src="006.jpg" width="100%" height="100%" >
                </div>
                <div class="tab-content" id="con3">
                    <img src="003.jpg" width="100%" height="100%" >
                </div>
                <div class="tab-content" id="con4">
                    <img src="004.jpg" width="100%" height="100%" >
                </div>
            </div>
            <ul class="listReset switch">
                <li><a href="javascript:;" id="tab1"><img src="icon1.png" width="20px" height="20px" ></a></li>
                <li><a href="javascript:;" id="tab2"><img src="icon2.png" width="20px" height="20px" ></a></li>
                <li><a href="javascript:;" id="tab3"><img src="icon3.png" width="20px" height="20px" ></a></li>
                <li><a href="javascript:;" id="tab4"><img src="icon4.png" width="20px" height="20px" ></a></li>
            </ul>
        </div>                
        <div id="content">
            <div class="box1">
                <img src="game2.jpg">
                <a href="https://dennishsiao.github.io/project/game.html"> 
                <div class="box1-hover-text">
                    <h2 class="box1-body">Game</h2>                    
                </div>
                </a> 
            </div>
            <div class="box2">
                <img src="0031.jpg">
                <a href="https://dennishsiao.github.io/project/video.html"> 
                <div class="box2-hover-text">
                    <h2 class="box2-body">Video</h2>                    
                </div>
                </a> 
            </div>
            <div class="box3">
                <img src="0061.jpg">
                <a href="https://dennishsiao.github.io/project/test.html"> 
                <div class="box3-hover-text">
                    <h2 class="box3-body">Test</h2>                    
                </div>
                </a> 
            </div>
        </div>
     
    </div>

</body>

</html>

