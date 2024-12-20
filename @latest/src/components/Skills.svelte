

<body>

    <h1>Skills and Technical Interests</h1>
    
        
    <div class="grid-container">
        <!-- Grid Element 1 -->
        <div class="grid-item">
            <h2>Cyber Security</h2>
            <p>I have experience with network security, penetration testing, and vulnerability assessments.</p>
            <button class="expand-btn" onclick="showOverlay('cyber')">Expand</button>
        </div>

        <!-- Grid Element 2 -->
        <div class="grid-item">
            <h2>Data Science & ML</h2>
            <p>Interested in data analysis and machine learning. Familiar with Jupyter, R, Pandas,</p>
            <button class="expand-btn" onclick="showOverlay('data')">Expand</button>
        </div>

        <!-- Grid Element 3 -->
        <div class="grid-item">
            <h2>Software Engineering</h2>
            <p>Development Cycle, Agile Process, Software Principles</p>
            <button class="expand-btn" onclick="showOverlay('data')">Expand</button>
        </div>

        <!-- Add more grid items as needed -->
    </div>

    <!-- Overlay for Cyber Security -->
    <div id="cyber" class="overlay">
        <div class="overlay-content">
            <span class="close-btn" onclick="hideOverlay('cyber')">&times;</span>
            <h2>Cyber Security</h2>
            <p>My deep knowledge in Cyber Security includes ethical hacking, network defense strategies, secure coding practices, and more.</p>
        </div>
    </div>

    <!-- Overlay for Data Science -->
    <div id="data" class="overlay">
        <div class="overlay-content">
            <span class="close-btn" onclick="hideOverlay('data')">&times;</span>
            <h2>Data Science</h2>
            <p>My experience in Data Science includes advanced Python programming, model building, and interpreting large datasets to generate insights.</p>
        </div>
    </div>

    <script>
        function showOverlay(id) {
            document.getElementById(id).style.display = 'block';
        }

        function hideOverlay(id) {
            document.getElementById(id).style.display = 'none';
        }
    </script>

</body>

<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

h1 {
    text-align: center;
    margin: 20px 0;
    color: #333;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
    padding: 20px;
    max-width: 100vw;
    margin: 0 auto;
}

.grid-item {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    
}

.grid-item h2 {
    font-size: 1.5rem;
    margin-bottom: 10px;
}

.grid-item p {
    font-size: 1rem;
    color: #666;
    margin-bottom: 20px;
}

.expand-btn {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.expand-btn:hover {
    background-color: #0056b3;
}

/* Overlay styles */
.overlay {
    display: none; /* Hidden by default */
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 1;
    justify-content: center;
    align-items: center;
}

.overlay-content {
    background-color: white;
    padding: 20px;
    max-width: 600px;
    margin: auto;
    text-align: center;
    border-radius: 8px;
    position: relative;
}

.overlay-content h2 {
    font-size: 2rem;
    margin-bottom: 10px;
}

.overlay-content p {
    font-size: 1rem;
    color: #666;
}

.close-btn {
    position: absolute;
    top: 10px;
    right: 20px;
    font-size: 2rem;
    cursor: pointer;
    color: #333;
}
</style>