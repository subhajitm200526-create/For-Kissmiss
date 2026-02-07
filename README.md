# For-Kissmiss
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Propose Day</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body {margin:0;height:100vh;background:linear-gradient(135deg,#ff5f6d,#ffc371);display:flex;justify-content:center;align-items:center;overflow:hidden;font-family:Arial;color:white;}
#rose {font-size:5rem;cursor:pointer;animation:pulse 1.5s infinite;}
@keyframes pulse{0%{transform:scale(1);}50%{transform:scale(1.2);}100%{transform:scale(1);}}
#messages {position:absolute;top:20%;width:100%;text-align:center;font-size:2rem;color:white;pointer-events:none;}
.heart {position:absolute;font-size:2rem;animation:float 5s linear infinite;}
@keyframes float{0%{bottom:-10%;opacity:1;}100%{bottom:110%;opacity:0;}}
</style>
</head>
<body>
<div id="rose">🌹</div>
<div id="messages"></div>
<script>
let messages=["💖 Happy Propose Day Kissmiss 💖","💘 Happy Propose Day Kissmiss 💘","💕 Happy Propose Day Kissmiss 💕"];
let msgIndex=0;
document.getElementById("rose").addEventListener("click",()=>{
  let msgDiv=document.createElement("div");
  msgDiv.textContent=messages[msgIndex%messages.length];
  msgIndex++;
  msgDiv.style.position="absolute";
  msgDiv.style.top=Math.random()*50+"vh";
  msgDiv.style.left=Math.random()*60+"vw";
  msgDiv.style.fontSize=(20+Math.random()*20)+"px";
  document.getElementById("messages").appendChild(msgDiv);
  setTimeout(()=>msgDiv.remove(),4000);
  for(let i=0;i<3;i++){
    let heart=document.createElement("div");
    heart.className="heart";
    heart.innerHTML="❤️💖💕";
    heart.style.left=Math.random()*100+"vw";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),5000);
  }
});
</script>
</body>
</html>
