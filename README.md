# Retro Arcade — Browser Games

クラシックアーケードを HTML5 Canvas で再現した、ブラウザだけで遊べるレトロゲーム集です。  
ビルド不要・インストール不要。HTML ファイルを開くだけでプレイできます。

## 収録タイトル

| ゲーム | ファイル | 説明 |
|--------|----------|------|
| **ASTEROIDS** | [`asteroids.html`](asteroids.html) | ベクター風 Asteroids クローン。パワーアップ・UFO・ホーミングミサイル付き |
| **Missile Command** | [`missile-command.html`](missile-command.html) | ミサイルコマンド風ディフェンスゲーム |

## 遊び方

### ローカルでプレイ

1. このリポジトリをクローンまたはダウンロード
2. 遊びたい HTML ファイルをブラウザで開く

```bash
git clone https://github.com/cookinglifehack-png/retro-browser-arcade-games.git
cd retro-browser-arcade-games
# Windows
start asteroids.html
# macOS
open asteroids.html
# Linux
xdg-open asteroids.html
```

または `index.html` を開いてメニューから選択してください。

### GitHub Pages で公開

1. GitHub リポジトリの **Settings → Pages**
2. **Source** を `main` ブランチ / `/ (root)` に設定
3. 公開 URL: `https://cookinglifehack-png.github.io/retro-browser-arcade-games/` にアクセス

## ASTEROIDS — 操作

| キー | 動作 |
|------|------|
| `↑` / `Space` | 前進 |
| `↓` | バック |
| `←` / `→` | 空間を回転（自機は常に上向き） |
| `X` | 通常弾 |
| `Z` | ホーミングミサイル（リロード制） |
| `P` | ポーズ |
| `Enter` / `Space` | スタート / リスタート |

### 主な特徴

- **固定自機 + 回転する宇宙** — 自機は画面下寄りに固定、周囲の空間が動く
- **5種類のパワーアップ**（各 Lv.4 まで・ランダム取得）
  - Fire Rate（連射速度）
  - Spread Shot（弾数）
  - Bullet Range（飛距離）
  - Homing Missiles（ミサイル数 1→5）
  - Orbiting Shields（防御オーブ）
- **出現率** — 強化が少ないほどパワーアップが出やすい（被弾で半減すると回復）
- **UFO** — プレイヤーの強化比率に応じて強弱が変化
- **被弾ペナルティ** — 全強化レベルが半分に（切り捨て）
- **残機 MAX 5** / ハイスコアは `localStorage` に保存
- **Web Audio API** によるレトロ SE・BGM

## 技術仕様

- 単一 HTML ファイル（CSS / JavaScript 内蔵）
- HTML5 Canvas 2D
- 外部依存: Google Fonts（Press Start 2P）のみ
- 対応ブラウザ: Chrome, Edge, Firefox, Safari などモダンブラウザ

## プロジェクト構成

```
.
├── index.html           # ゲーム選択メニュー（GitHub Pages 用）
├── asteroids.html       # ASTEROIDS
├── missile-command.html # Missile Command
├── README.md
└── .gitignore
```

## ライセンス

MIT License — 自由に利用・改変・配布できます。詳細は [LICENSE](LICENSE) を参照してください。

## 作者

[cookinglifehack-png](https://github.com/cookinglifehack-png) — 個人開発・学習用のプロジェクトです。Issue や Pull Request も歓迎します。