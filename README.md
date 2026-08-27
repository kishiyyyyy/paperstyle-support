# paperscreen-support

Paperscreen のサポートページとプライバシーポリシー。GitHub Pages がそのまま配信します。
ビルドはありません。手書きのHTMLとCSSだけです。

```
index.html          サポート（日英1ページ）
privacy/index.html  プライバシーポリシー（日英1ページ）
style.css           共通
```

アプリ本体は非公開の `kishiyyyyy/PaperScreen`。**判断の記録はそちらの `docs/decisions.md`
にあります。** ここには公開する文章だけを置きます。

## App Store Connect に入れる URL

| 欄 | URL |
| --- | --- |
| Support URL | `https://kishiyyyyy.github.io/paperscreen-support/` |
| Privacy Policy URL | `https://kishiyyyyy.github.io/paperscreen-support/privacy/` |

どちらも審査なしで差し替えられるメタデータです。独自ドメインに移しても再提出は要りません。

## LPと同居させない

LP（`PaperScreen` の #14）は別リポジトリにします。理由は2つです。

- LPはCanvasのデモを持つ予定で、静的サイトジェネレータを入れる可能性がある。生成器は
  出力を丸ごと作り直すので、手書きのページと同居すると消さない配慮が要り続ける
- **サポートURLが404だと審査で落ちます。** ガイドライン1.5で審査担当が実際に開くページです。
  LPは公開後も何度も触るので、そのデプロイと運命を共にさせない

このリポジトリは公開後ほぼコミットされない状態が正常です。

## やり残し

**`SUPPORT_EMAIL_HERE` を実際のアドレスに置き換えてください。** 4箇所あります。

```bash
grep -rn SUPPORT_EMAIL_HERE .
```

サポートURLに実際の連絡先が載っていることはガイドライン1.5の要件です。審査担当はiPhoneで
開くため、連絡先は最初の画面に入る位置に置いています。順番を変えないでください。

## 書くときのルール

日英を1ページに縦に並べます。言語ごとにファイルを分けると必ず片方が古くなるためです。

使ってはいけない表現（アプリ側の `AGENTS.md` と Issue #13 の表）:

- 日本の紙から着想した / 和柄、桜、富士山、筆文字
- AIが目に合わせて最適化する
- 眼精疲労が治る / 医学的に目を守る
- 9種類以上のテクスチャ
- 劇的に変わる / はっきり違う

アプリ名は `Paperscreen`。大文字は先頭の P だけです。
