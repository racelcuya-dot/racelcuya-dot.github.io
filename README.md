<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>GitHub School Demo</title>
    <style>
        body { font-family: -apple-system, BlinkMacSystemFont, sans-serif; max-width: 500px; margin: 50px auto; padding: 20px; }
        .card { border: 1px solid #e1e4e8; border-radius: 6px; padding: 20px; margin: 10px 0; }
        input { width: 100%; padding: 8px; margin: 5px 0; border: 1px solid #d0d7de; border-radius: 6px; }
        button { background: #2ea44f; color: white; padding: 10px 20px; border: none; border-radius: 6px; cursor: pointer; }
        .demo-repo { background: #f6f8fa; padding: 15px; border-radius: 6px; }
    </style>
</head>
<body>
    <h1>🎓 School GitHub Demo</h1>
    
    <div class="card">
        <h3>Create Demo Account Info</h3>
        <input type="text" id="ghuser" placeholder="GitHub Username (e.g., john-schoolproj)">
        <input type="password" id="ghpass" placeholder="Password (for demo only)">
        <button onclick="generateDemo()">Generate Demo Credentials</button>
        <div id="demo-output"></div>
    </div>

    <div class="card demo-repo">
        <h3>Sample Repo Link</h3>
        <p><strong>Share this with teacher:</strong></p>
        <code>https://github.com/<span id="repo-user">yourusername</span>/school-project</code>
    </div>

    <script>
        function generateDemo() {
            const user = document.getElementById('ghuser').value || 'student-demo-' + Math.floor(Math.random()*1000);
            const pass = document.getElementById('ghpass').value || 'DemoPass123!';
            
            document.getElementById('demo-output').innerHTML = `
                <p><strong>Demo GitHub Account:</strong></p>
                <strong>Username:</strong> ${user}<br>
                <strong>Password:</strong> ${pass}<br><br>
                <strong>Repo URL:</strong> https://github.com/${user}/school-project<br>
                <em>(Create real account manually, then share repo link only!)</em>
            `;
            document.getElementById('repo-user').textContent = user;
        }
        
        // Auto-generate example
        generateDemo();
    </script>
</body>
</html>
