# HTML/CSSを学ぶ

## Visual Studio Codeを使ってHTMLとCSSを書いてみる

### 基本的なHTMLの作成

まず、以下のコードをVisual Studio Codeに入力またはコピー&ペーストしてみましょう。ファイル名は`index.html`とします。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <title>Example Website</title>
</head>
<body>
これはウェブサイトです。
</body>
</html>
```

#### コードの説明

- `<!DOCTYPE html>`：この宣言は、ブラウザに対してこの文書がHTML5で書かれていることを伝えます。
- `<html lang="ja">`：HTML文書の開始を示します。`lang="ja"`はこの文書が日本語で書かれていることを示します。
- `<head>`：メタデータ（文書のタイトルやスタイル情報など）を含むセクションです。
  - `<title>Example Website</title>`：ウェブページのタイトルを指定します。ブラウザのタブやお気に入りに表示されます。
- `<body>`：実際にブラウザに表示されるコンテンツを含むセクションです。
  - `これはウェブサイトです。`：ブラウザに表示されるテキストです。
- 各タグには対応する終了タグがあります。例えば、`</body>`は`<body>`の終了を示します。

詳細な説明は、[MDNのチュートリアル](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web)を参照してください。

### 見出しやリンク、画像の追加

次に、ウェブページに見出しやリンク、画像を追加してみましょう。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <title>Example Website</title>
</head>
<body>

<h1>Example Website</h1>
<p>これはウェブサイトです。</p>

<ul>
  <li><a href="https://www.google.com/">Google</a></li>
  <li><a href="https://www.yahoo.co.jp/">Yahoo! JAPAN</a></li>
</ul>

<img src="computer01_smile.png" alt="笑顔のコンピューター">

</body>
</html>
```

#### コードの説明

- `<h1>Example Website</h1>`：大きな見出しを表示します。
- `<p>`：段落を示すタグです。テキストを段落として表示します。
- `<ul>`：順序なしリスト（箇条書き）を作成します。
  - `<li>`：リストの各項目を示します。
  - `<a href="URL">リンクテキスト</a>`：ハイパーリンクを作成します。`href`属性でリンク先のURLを指定します。
- `<img src="computer01_smile.png" alt="笑顔のコンピューター">`：画像を表示します。`src`属性で画像ファイルのパスを指定し、`alt`属性で画像が表示できない場合の代替テキストを指定します。

### CSSでスタイルを追加

ウェブページにスタイルを追加して、見た目を改善してみましょう。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <title>Example Website</title>
  <style>
    h1 {
      color: grey;
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

</body>
</html>
```

#### コードの説明

- `<style>`タグ：HTML内にCSSを記述するためのタグです。
- `h1 { color: grey; }`：`h1`タグのテキストカラーをグレーに設定します。

## 開発者コンソールの使い方

ブラウザの開発者コンソールを使うことで、ウェブページの構造やスタイルを確認・編集できます。

- **Chromeの場合**：ウェブページ上で右クリックし、「検証」を選択します。
- **Firefoxの場合**：ウェブページ上で右クリックし、「要素を検証」を選択します。

開発者コンソールを使って、リアルタイムでHTMLやCSSを編集し、変更を確認してみましょう。

## 発展課題

時間に余裕がある方は、以下のチャレンジに挑戦してみてください。

- **CSSを使ってデザインを改善**：背景色やフォントサイズ、レイアウトを変更して、ウェブページをより魅力的にしてみましょう。
- **新しいコンテンツを追加**：自分の好きな画像やリンク、文章を追加してオリジナルのページを作成してみてください。
- **外部CSSファイルを使ってみる**：スタイルをHTMLファイル内ではなく、別の`.css`ファイルに記述してリンクしてみましょう。
