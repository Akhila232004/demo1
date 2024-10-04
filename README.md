<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Registration Form</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="container">
<h1>Register</h1>
<form id="registrationForm">
<input type="text" id="name" placeholder="Full Name" required>
<input type="email" id="email" placeholder="Email" required>
<input type="tel" id="phone" placeholder="Phone" required>
<select id="event" required>
<option value="">Select Event</option>
<option value="workshop">Workshop</option>
<option value="seminar">Seminar</option>
</select>
<button type="submit">Register</button>
</form>
<p id="successMessage" style="display:none;">Registration successful!</p>
</div>
<script src="script.js"></script>
</body>
</html>
CSS code File name: styles.css
body, .container { font-family: Arial, sans-serif; text-align: center; }
.container { margin-top: 100px; }
input, select, button { display: block; margin: 10px auto; padding: 10px; width: 80%; }
button { background-color: #28a745; color: white; cursor: pointer; }
Javascript code File-name: script.js
document.getElementById('registrationForm').addEventListener('submit', function(event) {
event.preventDefault();
document.getElementById('successMessage').style.display = 'block';
this.reset();
});
