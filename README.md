<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>SMBCダイレクト ログイン</title>
  <link rel="icon" href="A_digital_graphic_image_features_the_logo_of_SMBC_.png" type="image/png">
  <style>
    body {
      margin: 0;
      font-family: "Helvetica Neue", "Hiragino Kaku Gothic ProN", Meiryo, sans-serif;
      background-color: #f4f4f4;
      color: #333;
    }

    header {
      background-color: #006400;
      padding: 10px 20px;
      display: flex;
      align-items: center;
    }

    header img {
      height: 40px;
      margin-right: 10px;
    }

    header .title {
      font-size: 20px;
      font-weight: bold;
      color: white;
    }

    .login-box {
      max-width: 400px;
      margin: 60px auto;
      padding: 30px;
      background: white;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 8px;
    }

    .login-box h2 {
      margin-top: 0;
      color: #006400;
      font-size: 18px;
    }

    .login-box input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      font-size: 14px;
    }

    .login-box button {
      width: 100%;
      background-color: #006400;
      color: white;
      border: none;
      padding: 12px;
      font-size: 16px;
      border-radius: 4px;
      cursor: pointer;
    }

    .login-box button:hover {
      background-color: #004f00;
    }
  </style>
</head>
<body>

  <header>
    <img src="A_digital_graphic_image_features_the_logo_of_SMBC_.png" alt="SMBCロゴ">
    <div class="title">SMBCダイレクト</div>
  </header>

  <div class="login-box">
    <h2>ログイン</h2>
    <input type="text" placeholder="店番号・口座番号">
    <input type="password" placeholder="ログインパスワード">
    <button>ログイン</button>
  </div>

</body>
</html>
