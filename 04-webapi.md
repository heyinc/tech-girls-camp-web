# Web APIを使って豪華なウェブサイトに

## PokeAPIを使って今日のラッキーポケモンを表示

以下のコードを使用して、PokeAPIからデータを取得し、ランダムなポケモンを表示してみましょう。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <title>Lucky Pokémon</title>
  <style>
    h1 {
      color: grey;
    }

    .pokemon {
      text-align: center;
    }

    .pokemon img {
      width: 200px;
    }
  </style>
</head>
<body>

<h1>今日のラッキーポケモン</h1>
<div class="pokemon">
  <h2 id="pokemonName"></h2>
  <img id="pokemonImage" src="" alt="ポケモンの画像">
</div>

<script>
  const pokemonName = document.getElementById('pokemonName');
  const pokemonImage = document.getElementById('pokemonImage');

  const randomId = Math.floor(Math.random() * 898) + 1; // ポケモンは現在898種

  fetch(`https://pokeapi.co/api/v2/pokemon/${randomId}`)
    .then(response => response.json())
    .then(data => {
      pokemonName.textContent = data.name;
      pokemonImage.src = data.sprites.front_default;
    })
    .catch(error => {
      console.error('エラーが発生しました:', error);
    });
</script>

</body>
</html>
```

### コードの説明

- `<div class="pokemon">`：ポケモンの情報を表示するコンテナです。
- `fetch()`：指定したURLからデータを取得します。
- `.then()`：非同期処理の結果を受け取って次の処理を行います。
- `data.name`：取得したポケモンの名前を取得します。
- `data.sprites.front_default`：ポケモンの画像URLを取得します。
- `Math.floor(Math.random() * 898) + 1`：1から898までのランダムな整数を生成します。

## 発展課題

さらにウェブAPIを活用して、以下のような機能を追加してみましょう。

- **OpenWeatherMap API**：現在の天気情報を取得して表示してみましょう。
  - [OpenWeatherMap API](https://openweathermap.org/api)
- **The Cat API**：ランダムな猫の画像を表示してみましょう。
  - [The Cat API](https://thecatapi.com/)
- **NASA API**：NASAが提供する天体写真を表示してみましょう。
  - [NASA API](https://api.nasa.gov/)

---

# 最後に

ワークショップはいかがでしたか？今回の内容を通して、ウェブ開発の基本からJavaScriptによる動的なコンテンツの追加、さらにウェブAPIを使った高度な機能の実装まで体験していただきました。

プログラミングやウェブ開発は、学べば学ぶほど新しい発見や楽しいことがたくさんあります。ぜひ引き続き学習を続けて、自分だけの素敵なウェブサイトを作ってみてください。

これからの皆さんの活躍を楽しみにしています！
