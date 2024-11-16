# JavaScriptを使ってもっと動くウェブサイトにしてみる

## 数当てゲームをサイトに組み込んでみる

以下のコードを`index.html`に追加または変更して、数当てゲームを実装してみましょう。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <title>Example Website</title>
  <style>
    h1 {
      color: grey;
    }

    .guessGame {
      margin: 20px;
    }

    .guessGame input {
      width: 100px;
    }
  </style>
</head>
<body>

<h1>Example Website</h1>
<p>これはウェブサイトです。</p>

<ul>
  <li><a href="https://www.google.com/">Google</a></li>
  <li><a href="https://www.yahoo.co.jp/">Yahoo! JAPAN</a></li>
</ul>

<img src="computer01_smile.png" alt="笑顔のコンピューター">

<div class="guessGame">
  <h2>数当てゲーム (1~20)</h2>
  <label for="guessField">予想: </label>
  <input type="number" min="1" max="20" id="guessField">
  <input type="submit" value="予想を入力" id="guessSubmit">
  <p id="guessResult"></p>
</div>

<script>
  const randomNumber = Math.floor(Math.random() * 20) + 1;
  console.log('正解は' + randomNumber);

  const guessField = document.querySelector('#guessField');
  const guessSubmit = document.querySelector('#guessSubmit');
  const guessResult = document.querySelector('#guessResult');

  function checkGuess() {
    const userGuess = Number(guessField.value);
    if (userGuess === randomNumber) {
      guessResult.textContent = '正解です！';
    } else if (userGuess < randomNumber) {
      guessResult.textContent = 'もっと大きいです';
    } else if (userGuess > randomNumber) {
      guessResult.textContent = 'もっと小さいです';
    }
  }

  guessSubmit.addEventListener('click', checkGuess);
</script>

</body>
</html>
```

### コードの説明

- `<div class="guessGame">`：数当てゲームのコンテナです。
- `<input type="number">`：数値を入力するためのフィールドです。
- `<input type="submit">`：ボタンをクリックして予想を送信します。
- `<p id="guessResult"></p>`：ゲームの結果やヒントを表示します。

#### JavaScript部分

- `Math.floor(Math.random() * 20) + 1`：1から20までのランダムな整数を生成します。
- `document.querySelector()`：指定したセレクタに一致する最初の要素を取得します。
- `function checkGuess()`：ユーザーの入力をチェックし、結果を表示する関数です。
- `addEventListener('click', checkGuess)`：ボタンがクリックされたときに`checkGuess`関数を呼び出します。

詳細な情報は、[MDNのJavaScript入門](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/JavaScript_basics)を参照してください。

## 発展課題

時間に余裕がある方は、以下の機能を追加してみてください。

- **試行回数の制限**：ユーザーが予想できる回数を制限し、ゲームオーバーの機能を追加してみましょう。
- **リセットボタンの実装**：ゲームを再度プレイできるように、リセットボタンを追加してみてください。
- **スタイルの改善**：CSSを使って、ゲーム部分の見た目をより良くしてみましょう。
