# デビエゴのゲーム置き場

AIで作った無料ブラウザゲームを公開するサイトです。GitHub Pages でそのまま公開できます。

## フォルダ構成

```
index.html            トップページ（ゲーム一覧・お知らせ）
about.html            このサイトについて
contact.html          お問い合わせ（XのDMへ案内）
privacy.html          プライバシーポリシー（AdSense用の文言入り）
style.css             全ページ共通のデザイン
img/                  サムネイル画像
games/slot-hall/
  index.html          ゲーム紹介ページ（遊び方・攻略・更新履歴）
  play.html           ゲーム本体
```

## 公開のしかた（GitHub Pages）

1. リポジトリの **Settings → Pages** を開く
2. Source を **Deploy from a branch**、Branch を **main / (root)** にして Save
3. 数分後に `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開される

## 新しいゲームを追加するとき

1. `games/<ゲーム名>/` フォルダを作り、`play.html`（ゲーム本体）と `index.html`（紹介ページ）を置く
   - 紹介ページは `games/slot-hall/index.html` をコピーして書き換えると楽
2. `img/` にサムネイル（横4:縦3）を置く
3. トップの `index.html` のゲーム一覧に `gcard` を1つ追加し、お知らせを1行追加

## AdSense を申し込むとき

- 申し込む前に、ゲームを何本か増やして紹介ページの文章も充実させておくと審査に通りやすい
- 審査用のコードは各ページの `<head>` 内（`index.html` の「AdSense：審査用コードはここ」の位置）に貼る
- 合格したら、ページ内の `<div class="ad-slot" ...></div>` の中に広告ユニットのコードを入れる（空のあいだは自動で非表示）
- ルートに `ads.txt` を置くよう案内されたら、AdSense の画面に出る1行をそのまま書いたファイルを作る
  - ※ `ユーザー名.github.io` のリポジトリでないと ads.txt をドメイン直下に置けないので注意
