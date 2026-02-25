index.html
login.html
register.html
dashboard.html
style.css
firebase.js
<script type="module">
import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js";
import { getAuth } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
</script>
<!DOCTYPE html>
<html>
<head>
<title>Register</title>
</head>
<body>

<h2>Register</h2>
<input type="email" id="email" placeholder="Email"><br><br>
<input type="password" id="password" placeholder="Password"><br><br>
<button onclick="register()">Register</button>

<script type="module">
import { auth } from './firebase.js';
import { createUserWithEmailAndPassword }
from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";

window.register = function(){
  const email = document.getElementById("email").value;
  const password = document.getElementById("password").value;

  createUserWithEmailAndPassword(auth, email, password)
  .then(() => {
    alert("Registered Successfully");
    window.location="login.html";
  })
  .catch((error)=> alert(error.message));
}
</script>

</body>
</html>
[00:20, 26/02/2026] .: <!DOCTYPE html>
<html>
<head>
<title>Register</title>
</head>
<body>

<h2>Register</h2>
<input type="email" id="email" placeholder="Email"><br><br>
<input type="password" id="password" placeholder="Password"><br><br>
<button onclick="register()">Register</button>

<script type="module">
import { auth } from './firebase.js';
import { createUserWithEmailAndPassword }
from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";

window.register = function(){
  const email = document.getElementById("email").value;
  const password = document.getElementById("password").value;

  createUserWithEmailAndPassword(auth, email, password)
  .then(() => {
    alert("Registered Successfully");
    window.location="login.html";
  })
  .catch((error)=> alert(error.message));
}
</script>

</body>
</html>
[00:21, 26/02/2026] .: <!DOCTYPE html>
<html>
<head>
<title>Login</title>
</head>
<body>

<h2>Login</h2>
<input type="email" id="email" placeholder="Email"><br><br>
<input type="password" id="password" placeholder="Password"><br><br>
<button onclick="login()">Login</button>

<script type="module">
import { auth } from './firebase.js';
import { signInWithEmailAndPassword }
from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";

window.login = function(){
  const email = document.getElementById("email").value;
  const password = document.getElementById("password").value;

  signInWithEmailAndPassword(auth, email, password)
  .then(() => {
    alert("Login Success");
    window.location="dashboard.html";
  })
  .catch((error)=> alert(error.message));
}
</script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Dashboard</title>
</head>
<body>

<h1>Welcome to E-Library 🎉</h1>
<button onclick="logout()">Logout</button>

<script type="module">
import { auth } from './firebase.js';
import { signOut }
from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";

window.logout = function(){
  signOut(auth).then(()=>{
    alert("Logged Out");
    window.location="login.html";
  });
}
</script>

</body>
</html
