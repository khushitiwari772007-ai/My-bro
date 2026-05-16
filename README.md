# My-bro
Some feelings of mine 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>For My Bhaiya</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family: 'Poppins', sans-serif;
    }

    body{
      overflow:hidden;
      background:black;
      color:white;
    }

    .container{
      width:100vw;
      height:100vh;
      position:relative;
    }

    .page{
      position:absolute;
      width:100%;
      height:100%;
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      text-align:center;
      padding:20px;
      opacity:0;
      transform:translateX(100%);
      transition:1s;
      background:black;
      overflow:hidden;
    }

    .page.active{
      opacity:1;
      transform:translateX(0);
    }

    h1{
      font-size:2.5rem;
      color:#ffd700;
      text-shadow:0 0 10px #ffd700;
      margin-bottom:25px;
      animation:glow 2s infinite alternate;
    }

    p{
      font-size:1.3rem;
      max-width:700px;
      line-height:1.8;
    }

    .btn{
      margin-top:40px;
      padding:12px 30px;
      border:none;
      border-radius:30px;
      background:#ffd700;
      color:black;
      font-size:1rem;
      cursor:pointer;
      transition:0.3s;
      font-weight:bold;
    }

    .btn:hover{
      transform:scale(1.1);
      box-shadow:0 0 20px #ffd700;
    }

    .stars{
      position:absolute;
      width:100%;
      height:100%;
      overflow:hidden;
      top:0;
      left:0;
      z-index:-1;
    }

    .star{
      position:absolute;
      width:3px;
      height:3px;
      background:white;
      border-radius:50%;
      animation:twinkle 2s infinite alternate;
    }

    @keyframes twinkle{
      from{
        opacity:0.2;
      }
      to{
        opacity:1;
        box-shadow:0 0 10px white;
      }
    }

    @keyframes glow{
      from{
        text-shadow:0 0 5px #ffd700;
      }
      to{
        text-shadow:0 0 20px #ffd700;
      }
    }

    .heart{
      font-size:3rem;
      color:#ffd700;
      margin-top:25px;
      animation:heartbeat 1.5s infinite;
    }

    @keyframes heartbeat{
      0%{transform:scale(1);}
      50%{transform:scale(1.2);}
      100%{transform:scale(1);}
    }

  </style>
</head>
<body>

<div class="container">

  <div class="stars" id="stars"></div>

  <div class="page active">
    <h1>To The Best Bhaiya ✨</h1>
    <p>
      I have never found someone who truly stayed beside me,
      until I found you.
      You became the comfort, support, and bond
      I always wished for.
    </p>
    <div class="heart">❤</div>
    <button class="btn" onclick="nextPage()">Next</button>
  </div>

  <div class="page">
    <h1>My Big Brother 💫</h1>
    <p>
      I will always consider you as my big brother.
      No matter what happens,
      this bond will always stay special for me.
    </p>
    <div class="heart">❤</div>
    <button class="btn" onclick="nextPage()">Next</button>
  </div>

  <div class="page">
    <h1>Always With You 🌙</h1>
    <p>
      I always want to stay beside you,
      support you,
      and be there for you
      as long as I live.
    </p>
    <div class="heart">❤</div>
    <button class="btn" onclick="nextPage()">Next</button>
  </div>

  <div class="page">
    <h1>Best Bhaiya Ever ❤️</h1>
    <p>
      You are my best brother,
      truly one of the most precious people in my life.
      I really love you so much, Bhaiya.
    </p>
    <div class="heart">❤</div>
  </div>

</div>

<script>

const pages = document.querySelectorAll('.page');
let currentPage = 0;

function nextPage(){
  pages[currentPage].classList.remove('active');
  currentPage++;
  if(currentPage < pages.length){
    pages[currentPage].classList.add('active');
  }
}

const starsContainer = document.getElementById('stars');

for(let i=0;i<200;i++){
  let star = document.createElement('div');
  star.classList.add('star');

  star.style.top = Math.random()*100 + '%';
  star.style.left = Math.random()*100 + '%';
  star.style.animationDuration = (Math.random()*3+1)+'s';

  starsContainer.appendChild(star);
}

</script>

</body>
</html>
