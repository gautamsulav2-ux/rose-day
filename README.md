<!DOCTYPE html>
<html>
<head>
    <title>Happy Rose Day</title>
    <style>
        body{
            margin:0;
            padding:0;
            font-family: Arial, Helvetica, sans-serif;
            text-align:center;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            overflow:hidden;
        }
        h1{
            margin-top:40px;
            color:white;
            font-size:50px;
            text-shadow:2px 2px 5px #ff4d6d;
        }
        p{
            font-size:22px;
            color:white;
        }
        .flower{
            font-size:100px;
            animation: float 3s infinite ease-in-out;
        }
        @keyframes float{
            0%{transform: translateY(0);}
            50%{transform: translateY(-20px);}
            100%{transform: translateY(0);}
        }
        .card{
            margin:40px auto;
            padding:20px;
            width:60%;
            background:white;
            border-radius:15px;
            box-shadow:0 0 20px pink;
        }
        button{
            padding:12px 25px;
            font-size:18px;
            border:none;
            border-radius:8px;
            background:#ff4d6d;
            color:white;
            cursor:pointer;
        }
        button:hover{
            background:#e60039;
        }

        /* Tulip pop animation */
        .tulip{
            position:absolute;
            font-size:40px;
            animation: pop 4s linear forwards;
        }
        @keyframes pop{
            0%{
                transform: scale(0) translateY(0);
                opacity:1;
            }
            50%{
                transform: scale(1.5) translateY(-150px);
            }
            100%{
                transform: scale(1) translateY(-300px);
                opacity:0;
            }
        }

        #message{
            color:red;
            font-size:22px;
            margin-top:20px;
            display:none;
        }

        footer{
            margin-top:40px;
            color:white;
            font-size:18px;
        }
    </style>
</head>

<body>

    <h1>🌷 Happy Rose Day 🌷</h1>

    <div class="flower">🌷</div>

    <div class="card">
        <h2>For Someone Very Special</h2>

        <button onclick="startTulips()">Click for Surprise</button>

        <p id="message">
            Just like this beautiful tulip, you bring color, joy, and warmth into my life.
            May your day bloom with happiness and smiles. 🌷
        </p>
    </div>

    <footer>
        Made with love on tulips 🌷
    </footer>

<script>
    function startTulips(){
        // show message
        document.getElementById("message").style.display = "block";

        // tulip animation
        for(let i=0;i<30;i++){
            let tulip = document.createElement("div");
            tulip.innerHTML = "🌷";
            tulip.className = "tulip";

            tulip.style.left = Math.random() * window.innerWidth + "px";
            tulip.style.top = window.innerHeight + "px";

            document.body.appendChild(tulip);

            setTimeout(() => {
                tulip.remove();
            }, 4000);
        }
    }
</script>

</body>
</html>
