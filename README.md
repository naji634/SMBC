<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>振り込め詐欺防止サイト</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>振り込め詐欺防止サイト</h1>
  </header>
  
  <main>
    <section>
      <h2>振込先番号確認ツール</h2>
      <form id="checkForm">
        <label for="bank">銀行名:</label>
        <input type="text" id="bank" name="bank" required>
        <label for="account">口座番号:</label>
        <input type="text" id="account" name="account" required>
        <button type="submit">確認</button>
      </form>
      <p id="result"></p>
    </section>

    <section>
      <h2>振込詐欺の実例</h2>
      <article>
        <h3>実例1: 偽の税務署からの通知</h3>
        <p>ある日、税務署を名乗る者から電話がかかってきました。詐欺師は税金の未納があると言い、すぐに振り込むように要求しました。しかし、公式な通知が来るまでは絶対に振り込まないようにしましょう。</p>
      </article>
    </section>

    <section>
      <h2>詐欺の兆候をチェックしよう</h2>
      <ul>
        <li>知らない番号からの電話がかかってきた。</li>
        <li>急に振込先が変更された。</li>
        <li>振込期限が非常に短い。</li>
        <li>支払い先が公式でない。</li>
      </ul>
    </section>

    <section>
      <h2>よくある質問</h2>
      <dl>
        <dt>振込先が本物か確認する方法は？</dt>
        <dd>公式の連絡手段で銀行に確認するのが最も安全です。</dd>
        <dt>詐欺に遭った場合、どうすればいい？</dt>
        <dd>すぐに警察に通報し、振込先の情報を提供してください。</dd>
      </dl>
    </section>

    <section>
      <h2>警告メッセージ</h2>
      <div id="warningBanner" style="background-color: red; color: white; padding: 10px; text-align: center;">
        <strong>警告！</strong> 振込先情報は必ず確認してください。疑わしい場合は、公式な連絡手段で確認しましょう。
      </div>
    </section>

    <section>
      <h2>振込詐欺防止のための動画</h2>
      <iframe width="560" height="315" src="https://www.youtube.com/embed/動画のID" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </section>

    <section>
      <h2>疑わしい振込先の例</h2>
      <p>以下は振込先として疑わしい例です。個人名の口座や、公式名義でない振込先は注意が必要です。</p>
      <ul>
        <li>個人名の口座</li>
        <li>公式名義ではない銀行名</li>
        <li>急に振込先が変更された</li>
      </ul>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 振り込め詐欺防止団体</p>
  </footer>

  <script>
    document.getElementById('checkForm').addEventListener('submit', function(event) {
      event.preventDefault();
      const bank = document.getElementById('bank').value;
      const account = document.getElementById('account').value;
      const result = document.getElementById('result');

      // 仮の確認処理（実際のAPIやデータベースと連携する場合）
      if (bank === '〇〇銀行' && account === '123-456-789') {
        result.textContent = 'この振込先は正しい銀行です。';
      } else {
        result.textContent = '警告：この振込先は確認できませんでした。';
      }
    });
  </script>
</body>
</html>
