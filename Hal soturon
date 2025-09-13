<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>製品レコメンド</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f2f2f2; /* 白〜グレー */
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
    }

    /* ヘッダー */
    header {
      width: 100%;
      background: #111;
      color: #fff;
      padding: 15px 25px;
      font-size: 1.3em;
      font-weight: bold;
      text-align: left;
    }

    /* コンテナ */
    .container {
      background: #fff;
      border-radius: 12px;
      padding: 30px;
      max-width: 1000px;
      width: 90%;
      margin-top: 40px;
      box-shadow: 0 6px 16px rgba(0,0,0,0.2);
      text-align: center;
    }

    /* 項目全体を横並び */
    .questions {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      margin-bottom: 30px;
    }

    .question {
      flex: 1;
      padding: 15px;
      border: 1px solid #ddd;
      border-radius: 10px;
      background: #fafafa;
      text-align: left;
    }

    .question p {
      font-weight: bold;
      margin-bottom: 10px;
      color: #222;
      font-size: 1.05em;
    }

    label {
      display: block;
      margin: 6px 0;
      cursor: pointer;
      font-size: 0.95em;
    }

    button {
      background: #111;
      color: #fff;
      border: none;
      padding: 12px 25px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      transition: 0.3s;
    }

    button:hover {
      background: #333;
    }

    .recommend {
      margin-top: 30px;
      padding: 20px;
      border-radius: 10px;
      background: #f9f9f9;
      text-align: left;
    }

    .product {
      margin-bottom: 20px;
    }

    .product h3 {
      margin: 0;
      font-size: 1.2em;
      color: #111;
    }

    .product p {
      margin: 5px 0;
      color: #444;
    }

    .review {
      font-style: italic;
      color: #666;
    }
  </style>
</head>
<body>
  <!-- ヘッダー -->
  <header>
    製品レコメンド
  </header>

  <div class="container">
    <!-- 横並びの質問 -->
    <div class="questions">
      <!-- 音質 -->
      <div class="question">
        <p>好みの音質:</p>
        <label><input type="radio" name="sound" value="重低音"> 重低音</label>
        <label><input type="radio" name="sound" value="高音クリア"> 高音クリア</label>
        <label><input type="radio" name="sound" value="バランス型"> バランス型</label>
      </div>

      <!-- 使い心地 -->
      <div class="question">
        <p>使い心地:</p>
        <label><input type="radio" name="comfort" value="軽量"> 軽量</label>
        <label><input type="radio" name="comfort" value="遮音性重視"> 遮音性重視</label>
        <label><input type="radio" name="comfort" value="長時間使用"> 長時間使用</label>
      </div>

      <!-- こだわり -->
      <div class="question">
        <p>こだわり:</p>
        <label><input type="radio" name="feature" value="ワイヤレス"> ワイヤレス</label>
        <label><input type="radio" name="feature" value="ハイレゾ対応"> ハイレゾ対応</label>
        <label><input type="radio" name="feature" value="デザイン性"> デザイン性</label>
      </div>
    </div>

    <!-- ボタンは下に -->
    <div>
      <button onclick="recommend()">おすすめを見る</button>
    </div>

    <div id="result" class="recommend"></div>
  </div>

  <script>
    const products = [
      {
        name: "Sony WH-1000XM5",
        description: "ソニーのフラッグシップノイズキャンセリングヘッドホン。",
        review: "ノイズキャンセリング性能が最高で、飛行機や電車でも快適。低音も深みがあり長時間使用でも疲れにくいと高評価。"
      },
      {
        name: "Audio-Technica ATH-M50x",
        description: "プロも愛用するモニターヘッドホン。",
        review: "音の解像度が高く、バランスが良い。中音域のクリアさを評価する声多数。ただし長時間だと少し重さを感じる人も。"
      },
      {
        name: "Bose QuietComfort 45",
        description: "ボーズの定番ノイズキャンセリングモデル。",
        review: "装着感が柔らかく、飛行機移動に最適との声多数。音質はフラット寄りで聴き疲れしにくい点が人気。"
      }
    ];

    function recommend() {
      const sound = document.querySelector('input[name="sound"]:checked');
      const comfort = document.querySelector('input[name="comfort"]:checked');
      const feature = document.querySelector('input[name="feature"]:checked');
      const resultDiv = document.getElementById('result');

      if (!sound || !comfort || !feature) {
        resultDiv.innerHTML = "<p style='color:red;'>すべての項目を選択してください。</p>";
        return;
      }

      // サンプルとして全商品を表示
      resultDiv.innerHTML = `
        <h2>おすすめ製品</h2>
        ${products.map(p => `
          <div class="product">
            <h3>${p.name}</h3>
            <p>${p.description}</p>
            <p class="review">💬 レビュー要約: ${p.review}</p>
          </div>
        `).join("")}
      `;
    }
  </script>
</body>
</html>
