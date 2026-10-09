# AI時代の教育を考える

学生自主ゼミの募集サイト。HTML・CSSのみで動作し、既存サイトのテンプレートやランタイムは使用しません。

## 開発

```sh
npm ci
npm run dev
npm run check
```

掲載内容は `public/index.html` を編集します。FAQは標準の `<details>` で開閉します。

## Cloudflare Workers

- Worker: `ut-ai-education`
- Account: `nextgeneration-education`
- 公開URL: https://ut-ai-education.nextgeneration-education.workers.dev/
- 配信ディレクトリ: `public`

初回は2026年10月9日にCloudflareダッシュボードから静的ファイルを直接アップロードして登録しました。Git自動ビルド連携は未設定です。

対象アカウントで認証後、`npm run deploy` で配信します。ダッシュボードから `public` の内容をアップロードする方法でも登録できます。

Workers Buildsを設定する場合:

- GitHub: `nextgeneration-education-org/ut-ai-education`
- Branch: `main`
- Root directory: `/`
- Build command: 空欄（ビルド不要）
- Deploy command: `npm run deploy`
- Preview command: `npx wrangler versions upload`

## 掲載情報

2026年10月9日に確認したInstagram `@ut_ai_education` を優先。
初回2026/10/19、月曜18:45–20:30、全12回予定、教育学部棟3階、定員15名、無料、10/15申込締切。
小学生向けイベントはInstagramの1/16（土）と開催時期から2027/1/16（土・予定）として掲載。
現場活動の頻度・参加条件、ゲスト・教材の詳細は準備中。

最新情報: https://www.instagram.com/ut_ai_education/
参加フォーム: https://forms.gle/gkLQQfbvXLFWKv9V8

## 写真素材

ドライブ提供写真から、掲載同意が未確認のため顔・名札を含まない手元のみを切り出しています。原本は公開リポジトリに保存しません。

- `learning-hands.jpg`: じゆうラボ記録写真 `P1032012.JPG`（Drive ID: `1M7VwhXPeMbjKjCAOQCDOiooKIo9CeY7x`）
- `exploration-hands.jpg`: はっけんラボ記録写真 `IMG_8072.JPG`（Drive ID: `1cfhIOsu8DvFSg4NoF8J2JZNwDrlbJQWs`）

現場の学びを伝えるイメージ写真として使用しています。ゼミの実施記録を示すキャプションは付けていません。JPEGとして軽量化し、EXIFを削除済みです。
