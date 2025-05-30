# ゲームルール定義 - 豆腐のテトリス

## 操作方法（基本）

| 操作       | キー/入力方法 | 説明                             |
|------------|---------------|----------------------------------|
| 左に移動   | ←             | ピースを左へ1マス移動           |
| 右に移動   | →             | ピースを右へ1マス移動           |
| 下に落下   | ↓             | ピースを1段早く落とす           |
| 回転       | ↑ または Z    | ピースを90度回転（時計回り）    |
| ハードドロップ | スペースキー   | 一気に一番下まで落とす         |
| ポーズ     | P             | 一時停止                        |

---

## ゲームの進行ルール

- ピースはランダムに1つずつ生成される
- ピースが着地したら固定され、**崩壊判定が行われる**
- 横一列が埋まった場合は**その行が消える**
- 崩壊ルールによって豆腐がズレ落ちると、**再着地→再崩壊の連鎖が発生**する可能性あり

---

## スコアリング

| アクション         | 得点       |
|--------------------|------------|
| 横一列消去         | 100 点     |
| 連鎖崩壊1回        | 150 点     |
| 連鎖崩壊2回以上     | +50 点ずつ加算 |
| ハードドロップ成功 | 50 点      |

---

## ゲームオーバー条件

- 新しいピースが**画面上部で配置できなかった場合**
- 一定時間操作しなかった場合（タイムアウト、オプション）

---

## 難易度調整（将来的な実装）

- ピース落下速度の段階的上昇
- スコアに応じて「特殊ピース」出現
- 視覚効果・サウンドの強化
