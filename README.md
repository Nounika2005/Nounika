<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Nounika</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        
        .card {
            max-width: 500px;
            width: 100%;
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeIn 0.6s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .profile-header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .avatar {
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            color: white;
            margin: 0 auto 15px;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }
        
        h2 { 
            color: #333;
            margin-bottom: 5px;
            font-size: 28px;
        }
        
        .college {
            color: #667eea;
            font-size: 14px;
            font-weight: 600;
            letter-spacing: 1px;
        }
        
        .info-section {
            margin: 20px 0;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }
        
        .info-label {
            font-weight: 600;
            color: #667eea;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 8px;
        }
        
        .info-content {
            color: #333;
            line-height: 1.6;
            font-size: 15px;
        }
        
        .btn {
            padding: 12px 24px;
            margin-top: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            width: 100%;
            font-size: 16px;
            font-weight: 600;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        #customBio {
            display: none;
            margin-top: 15px;
        }
        
        textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-family: inherit;
            font-size: 14px;
            resize: vertical;
            min-height: 80px;
            transition: border-color 0.3s;
        }
        
        textarea:focus {
            outline: none;
            border-color: #667eea;
        }
        
        .btn-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        .btn-small {
            padding: 8px 16px;
            flex: 1;
            font-size: 14px;
        }
        
        .btn-secondary {
            background: #6c757d;
        }
        
        .btn-secondary:hover {
            box-shadow: 0 5px 15px rgba(108, 117, 125, 0.4);
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="profile-header">
            <div class="avatar">N</div>
            <h2 id="name">Nounika</h2>
            <p class="college">PSGRKCW</p>
        </div>
        
        <div class="info-section">
            <div class="info-label">About Me</div>
            <div class="info-content" id="bio">
                I am a creative and passionate student at PSG R. Krishnammal College for Women. 
                I love exploring technology, building innovative projects, and constantly learning new things. 
                My interests include web development, programming, and creating solutions that make a difference.
            </div>
        </div>
        
        <div class="info-section">
            <div class="info-label">Interests</div>
            <div class="info-content">
                💻 Web Development • 🎨 Creative Design • 📚 Continuous Learning • 🚀 Innovation
            </div>
        </div>
        
        <button class="btn" onclick="toggleBioEdit()">Edit Bio</button>
        
        <div id="customBio">
            <textarea id="bioInput" placeholder="Write something about yourself..."></textarea>
            <div class="btn-group">
                <button class="btn btn-small" onclick="saveBio()">Save</button>
                <button class="btn btn-small btn-secondary" onclick="cancelEdit()">Cancel</button>
            </div>
        </div>
    </div>
    
    <script>
        let originalBio = document.getElementById("bio").innerText;
        
        function toggleBioEdit() {
            const customBio = document.getElementById("customBio");
            const bioInput = document.getElementById("bioInput");
            
            customBio.style.display = "block";
            bioInput.value = document.getElementById("bio").innerText;
            bioInput.focus();
        }
        
        function saveBio() {
            const newBio = document.getElementById("bioInput").value.trim();
            
            if(newBio) {
                document.getElementById("bio").innerText = newBio;
                originalBio = newBio;
            }
            
            cancelEdit();
        }
        
        function cancelEdit() {
            document.getElementById("customBio").style.display = "none";
        }
    </script>
</body>
</html>
