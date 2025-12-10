# Nounika
Hello This is Nounika PSGRKCW
<!DOCTYPE html>
<html>
<head>
    <title>About Nounika</title>
    <style>
        body { font-family: Arial; background: #f9f9f9; padding: 20px; }
        .card {
            max-width: 400px; margin: auto; background: white;
            padding: 20px; border-radius: 10px; box-shadow: 0 0 10px #ccc;
        }
        h2 { text-align: center; }
        .btn {
            padding: 8px 12px; margin-top: 10px;
            background: #6200ee; color: white; border: none;
            border-radius: 5px; cursor: pointer; width: 100%;
        }
        #bio { margin-top: 10px; }
    </style>
</head>
<body>

<div class="card">
    <h2>About Me - Nounika</h2>

    <p><strong>Name:</strong> <span id="name">NOUNIKA</span></p>

    <p><strong>Bio:</strong></p>
    <p id="bio">I am a creative learner who loves technology and building cool projects.</p>

    <button class="btn" onclick="changeBio()">Change Bio</button>
</div>

<script>
function changeBio() {
    let newBio = prompt("Enter your new bio:");
    if(newBio) {
        document.getElementById("bio").innerText = newBio;
    }
}
</script>

</body>
</html>
