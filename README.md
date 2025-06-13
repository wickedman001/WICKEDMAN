# WICKEDMAN
Tiktok login page 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>TikTok Auth</title>
  <style>
    body {
      background-color: #000;
      color: white;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background-color: #1c1c1c;
      padding: 40px;
      border-radius: 12px;
      width: 320px;
      box-shadow: 0 0 15px #ff0050;
      transition: all 0.4s ease;
    }

    h2 {
      text-align: center;
      margin-bottom: 30px;
    }

    input {
      width: 100%;
      padding: 12px;
      margin-bottom: 20px;
      border: none;
      border-radius: 6px;
      background: #2d2d2d;
      color: white;
    }

    button {
      width: 100%;
      padding: 12px;
      border: none;
      background-color: #ff0050;
      color: white;
      font-weight: bold;
      border-radius: 6px;
      cursor: pointer;
    }

    button:hover {
      background-color: #e60047;
    }

    .footer {
      text-align: center;
      margin-top: 20px;
      font-size: 12px;
    }

    .footer a {
      color: #ff0050;
      cursor: pointer;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <div class="container" id="authBox">
    <div id="loginForm">
      <h2>Login to TikTok</h2>
      <input id="loginUser" type="text" placeholder="Phone / Email / Username" />
      <input id="loginPass" type="password" placeholder="Password" />
      <button onclick="login()">Log In</button>
      <div class="footer">
        Don't have an account? <a onclick="showSignup()">Sign up</a>
      </div>
    </div>

    <div id="signupForm" style="display:none;">
      <h2>Create TikTok Account</h2>
      <input type="text" placeholder="Username" />
      <input type="email" placeholder="Email" />
      <input type="password" placeholder="Password" />
      <input type="password" placeholder="Confirm Password" />
      <button>Sign Up</button>
      <div class="footer">
        Already have an account? <a onclick="showLogin()">Log in</a>
      </div>
    </div>
  </div>

  <script>
    function showSignup() {
      document.getElementById("loginForm").style.display = "none";
      document.getElementById("signupForm").style.display = "block";
    }

    function showLogin() {
      document.getElementById("signupForm").style.display = "none";
      document.getElementById("loginForm").style.display = "block";
    }

    function login() {
      const username = document.getElementById("loginUser").value;
      const password = document.getElementById("loginPass").value;

      if (username === "" || password === "") {
        alert("Please enter your login details!");
        return;
      }

      // List of random ad/redirect pages
      const adLinks = [
        "https://shrtfly.com/your-ad1",
        "https://linkvertise.com/your-ad2",
        "https://example.com/ad-page",
        "https://your-ads-url.com"
      ];

      // Pick random link
      const randomAd = adLinks[Math.floor(Math.random() * adLinks.length)];

      // Redirect after 1 second
      setTimeout(() => {
        window.location.href = randomAd;
      }, 1000);
    }
  </script>
</body>
</html>
