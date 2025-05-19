# クラス構造設計 - 豆腐のテトリス

## 🎮 主なクラスと責務（責任）

### `GameEngine`
- ゲームの進行管理、ゲームループ
- ピース生成、タイミング制御、スコア更新

### `GameBoard`
- 盤面の状態（2次元配列）
- ブロックの配置管理
- 横一列の消去・崩壊処理のトリガー

### `Piece`
- ピースの形状、座標、回転状態
- 自身の移動・回転の判定

### `PieceFactory`
- ランダムにピースを生成
- 初期位置をセットする

### `CollisionChecker`
- ピースが移動可能か、接触するかの判定

### `CollapseHandler`
- 3個以上の連結を検出
- 崩壊部分の特定とスライド処理

---

## 🧱 クラスの関連イメージ図
GameEngine
├─ PieceFactory
├─ GameBoard
│ ├─ CollisionChecker
│ └─ CollapseHandler
└─ Piece


---

## 🧠 今後追加の可能性があるクラス

- `SoundManager`：効果音など
- `UIController`：スコアやポーズ画面の描画
- `InputHandler`：キーボード・タッチ操作の処理

---

## 📌 補足メモ

- 各クラスは TypeScript の `class` or `interface` で定義予定
- ファイル分割単位：`src/GameEngine.ts`, `src/Piece.ts`, `src/Board.ts` など
