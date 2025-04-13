<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>振込先ローダリングサイト</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>振込先ローダリングサイト</h1>
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
      <h2>マネーロンダリングとは</h2>
      <article>
        <h3>マネーロンダリングの概要</h3>
        <p>マネーロンダリングとは、不正に得たお金を合法的に見せかけるために行われる一連の行為のことです。犯罪者は違法な手段で得たお金を「洗浄」することで、警察や監視機関の目を逃れようとします。例えば、振込先を使って不正に得た資金を他のアカウントに転送するなどの手法が取られます。</p>
      </article>
    </section>

    <section>
  <h2>よくある質問</h2>
  <dl>
    <dt>振込先が本物か確認する方法は？</dt>
    <dd>公式の連絡手段で銀行に確認するのが最も安全です。</dd>

    <dt>登録するとビットコイン50,000円分もらえるって本当？</dt>
    <dd>一部のサイトでは、ウォレットアドレスを登録すると自動的にビットコインがもらえるとされています。これはよくある詐欺の手口で、情報を盗まれる危険があります。本FAQの内容は教育用のフィクションです。</dd>

    <dt>マネーロンダリングとは何ですか？</dt>
    <dd>
      マネーロンダリングとは、犯罪などで得た資金の出どころを隠し、正当な収入に見せかける行為です。一般的に3つの段階に分けられます：
      <ol>
        <li><strong>置換（Placement）</strong> - 現金を銀行などの金融機関に預ける段階。</li>
        <li><strong>分散（Layering）</strong> - 資金の出所を分かりにくくするために、複数の取引や国際送金などを通して分散させる段階。</li>
        <li><strong>統合（Integration）</strong> - 最終的に“正当な”資金として表に出す段階。</li>
      </ol>
    </dd>

    <dt>情報を入力するとビットコインが入るって本当？</dt>
    <dd>
      一部の詐欺サイトでは、ウォレットアドレスを登録すると資金が入ると宣伝されていますが、これは信用してはいけません。こうした仕組みは実在しません。本FAQ内の記述は詐欺の手口を学ぶためのフィクションです。
    </dd>

    <dt>このサイトを使って大丈夫？</dt>
    <dd>
      braveなどの匿名性の高いブラウザを利用することで追跡リスクは下がる可能性がありますが、個人情報の取扱いについては慎重に判断してください。本サイトの内容は学習・教育目的のものであり、実際の取引を勧めるものではありません。
    </dd>
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
