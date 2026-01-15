
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Treasure Hunt for My Love ❤️</title>
<style>
body {
    margin:0;
    font-family:'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #ff9a9e, #ff6f91);
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    color:white;
    text-align:center;
}
.card {
    background: rgba(255,255,255,0.15);
    padding: 40px;
    border-radius: 20px;
    width: 90%;
    max-width: 450px;
    box-shadow: 0 0 20px rgba(0,0,0,0.3);
}
input {
    padding:12px;
    width:75%;
    border:none;
    border-radius:10px;
    margin-top:20px;
    outline:none;
}
button {
    padding:12px 25px;
    border:none;
    border-radius:20px;
    background:#fff;
    color:#ff416c;
    font-weight:bold;
    margin-top:10px;
    cursor:pointer;
}
button:hover {
    background:#ffe6eb;
}
.heart {
    font-size:40px;
    animation:beat 1s infinite;
}
@keyframes beat{
    0%,100%{transform:scale(1);}
    50%{transform:scale(1.2);}
}
</style>
</head>
<body>

<div class="card" id="box">
    <h2>💌 Online Love Treasure Hunt</h2>
    <p id="text">
        Clue 1 💬 <br>
        Apki pehli call kab hui thi?
    </p>
    <input type="text" id="answer" placeholder="Enter your answer...">
    <br>
    <button onclick="check()">Next</button>
</div>

<script>
let step = 0;

// Personalized answers
const answers = [
    "19 april 2025",
    "19 march 2025",
    "jaan",
    "😒"
];

function check() {
    let input = document.getElementById("answer").value.toLowerCase().trim();

    if(input === answers[step].toLowerCase()) {
        step++;
        if(step === 1) {
            show("Clue 2 🌹<br>Apko first time propose kab kiya gaya tha?");
        } else if(step === 2) {
            show("Clue 3 😄<br>Ap mujhe zyada kis naam se bulate ho?");
        } else if(step === 3) {
            show("Clue 4 😠<br>Ap gussay me konsa emoji use karti ho?");
        } else {
            document.getElementById("box").innerHTML = `
                <h1 class="heart">❤️</h1>
                <h2>I LOVE YOU</h2>
                <p>
                Hum mile nahi, magar tum meri zindagi ka <br>
                sabse khoobsurat hissa ho 💕
                </p>
            `;
        }
    } else {
        alert("Oops! Thora socho… ❤️");
    }
}

function show(text) {
    document.getElementById("text").innerHTML = text;
    document.getElementById("answer").value = "";
    document.getElementById("answer").placeholder = "Type your answer...";
}
</script>

</body>
</html>
