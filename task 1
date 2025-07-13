<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Grade Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Student Grade Calculator</h1>

        <div class="input-group">
            <label for="maths">Maths Marks (out of 100):</label>
            <input type="number" id="maths" min="0" max="100" value="0">
        </div>

        <div class="input-group">
            <label for="science">Science Marks (out of 100):</label>
            <input type="number" id="science" min="0" max="100" value="0">
        </div>

        <div class="input-group">
            <label for="english">English Marks (out of 100):</label>
            <input type="number" id="english" min="0" max="100" value="0">
        </div>

        <div class="input-group">
            <label for="history">History Marks (out of 100):</label>
            <input type="number" id="history" min="0" max="100" value="0">
        </div>

        <div class="input-group">
            <label for="computer">Computer Marks (out of 100):</label>
            <input type="number" id="computer" min="0" max="100" value="0">
        </div>

        <button id="calculateBtn" onclick="calculateGrade()">Calculate Grade</button>

        <div id="results">
            <h2>Results:</h2>
            <p><strong>Total Marks:</strong> <span id="totalMarks">0</span></p>
            <p><strong>Average Percentage:</strong> <span id="averagePercentage">0.00%</span></p>
            <p><strong>Grade:</strong> <span id="grade">N/A</span></p>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
<html>
<style>

body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f4f4f4;
    margin: 0;
}

.container {
    background-color: #fff;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 100%;
    max-width: 500px;
}

h1 {
    color: #333;
    margin-bottom: 25px;
}

.input-group {
    margin-bottom: 15px;
    text-align: left;
}

.input-group label {
    display: block;
    margin-bottom: 5px;
    color: #555;
    font-weight: bold;
}

.input-group input[type="number"] {
    width: calc(100% - 20px);
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 16px;
}

button {
    background-color: #007bff;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 18px;
    margin-top: 20px;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

#results {
    margin-top: 30px;
    padding-top: 20px;
    border-top: 1px solid #eee;
    text-align: left;
}

#results h2 {
    color: #333;
    margin-bottom: 15px;
    text-align: center;
}

#results p {
    font-size: 18px;
    margin-bottom: 10px;
    color: #444;
}

#results p strong {
    color: #007bff;
}

#totalMarks, #averagePercentage, #grade {
    font-weight: normal;
    color: #28a745; /* Green for success */
}

#grade {
    font-weight: bold;
    color: #dc3545; /* Red for emphasis, or change based on grade */
}
</style>
</html>
<script>
function calculateGrade() {
    // Get input values
    const mathsMarks = parseFloat(document.getElementById('maths').value);
    const scienceMarks = parseFloat(document.getElementById('science').value);
    const englishMarks = parseFloat(document.getElementById('english').value);
    const historyMarks = parseFloat(document.getElementById('history').value);
    const computerMarks = parseFloat(document.getElementById('computer').value);

    // Validate inputs
    if (isNaN(mathsMarks) || isNaN(scienceMarks) || isNaN(englishMarks) || isNaN(historyMarks) || isNaN(computerMarks) ||
        mathsMarks < 0 || mathsMarks > 100 ||
        scienceMarks < 0 || scienceMarks > 100 ||
        englishMarks < 0 || englishMarks > 100 ||
        historyMarks < 0 || historyMarks > 100 ||
        computerMarks < 0 || computerMarks > 100) {
        alert("Please enter valid marks between 0 and 100 for all subjects.");
        document.getElementById('totalMarks').textContent = '0';
        document.getElementById('averagePercentage').textContent = '0.00%';
        document.getElementById('grade').textContent = 'Invalid Input';
        return;
    }

    // Calculate total marks
    const totalMarks = mathsMarks + scienceMarks + englishMarks + historyMarks + computerMarks;

    // Calculate average percentage (assuming 5 subjects, each out of 100)
    const numberOfSubjects = 5;
    const maxTotalMarks = numberOfSubjects * 100;
    const averagePercentage = (totalMarks / maxTotalMarks) * 100;

    // Determine the grade
    let grade;
    if (averagePercentage >= 90) {
        grade = 'A+';
    } else if (averagePercentage >= 80) {
        grade = 'A';
    } else if (averagePercentage >= 70) {
        grade = 'B';
    } else if (averagePercentage >= 60) {
        grade = 'C';
    } else if (averagePercentage >= 50) {
        grade = 'D';
    } else {
        grade = 'F';
    }

    // Display results
    document.getElementById('totalMarks').textContent = totalMarks;
    document.getElementById('averagePercentage').textContent = averagePercentage.toFixed(2) + '%';
    document.getElementById('grade').textContent = grade;

    // Optional: Change grade color based on result
    const gradeElement = document.getElementById('grade');
    if (grade === 'F') {
        gradeElement.style.color = '#dc3545'; // Red
    } else if (grade === 'A+' || grade === 'A') {
        gradeElement.style.color = '#28a745'; // Green
    } else {
        gradeElement.style.color = '#ffc107'; // Yellow/Orange
    }
}
