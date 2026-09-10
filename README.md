# 公開フォルダ（GitHub Pages にそのまま上げる）

このフォルダの中身を、そのままリポジトリのルートに置いてください。

```
index.html          読者が最初に開くページ（音声とアプリの入口）
app/index.html      練習アプリ
audio/第01課/*.mp3  本文の音声（12課 × 7トラック）
audio/テスト/*.mp3   確認テストと総合模擬テストの音声
```

## 手順
1. GitHubで新しいリポジトリを作る（例: `chinese-cuisine`）。公開（Public）にします。
2. このフォルダの中身をすべてアップロードする（`README.md` は不要）。
3. Settings → Pages → Deploy from a branch → `main` / `(root)` → Save。
4. 数分後、`https://<ユーザー名>.github.io/chinese-cuisine/` で開きます。
5. そのURLで本のQRコードを作り直します。

```bash
python3 ~/.claude/skills/tanbun-cuisine-lesson/scripts/build_front.py . "https://<ユーザー名>.github.io/chinese-cuisine/"
```

これで `04_画像/QR_アプリと音声.png` と前付けレイアウトのQRが実URLに差し替わります。

## 容量
音声を含めて約33MB。GitHub Pages の推奨上限（1リポジトリ1GB）に対して十分小さい容量です。
