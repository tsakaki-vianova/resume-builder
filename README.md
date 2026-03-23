# 履歴書・職務経歴書 作成ツール

ブラウザだけで完結する無料の履歴書・職務経歴書作成Webアプリです。
厚生労働省様式例（2021年4月〜）に準拠した体裁の整ったExcel（.xlsx）ファイルを出力できます。

**デモ・公開URL:** https://via-nova.jp/resume-builder/

---

## 特徴

- **サーバー不要** — 単一のHTMLファイル（`index.html`）で動作。ローカルでも使える
- **Excel（.xlsx）出力** — 競合サービスの多くはPDFのみ。このツールはExcelで出力するため、再編集・微修正が容易
- **PDF・Wordからインポート** — 既存の職務経歴書（PDF/Word）をアップロードするとテキストを自動抽出
- **テンプレート方式** — `templates/` フォルダのExcelテンプレートをベースに帳票を生成。レイアウトの精緻化が容易

## 機能一覧

### 履歴書
- 氏名・ふりがな・生年月日（年齢自動計算）・住所・連絡先・メール
- 学歴・職歴の動的追加/削除
- 免許・資格（複数行対応）
- 志望動機・本人希望記入欄
- Excel（.xlsx）ダウンロード

### 職務経歴書
- 職務要約・スキルセット
- 会社ごとの在籍期間・規模・事業内容・職種
- プロジェクト単位の業務詳細・実績・使用技術
- 自己PR
- Excel（.xlsx）ダウンロード

### 共通
- PDF・Word（.docx）ファイルのアップロードでテキスト自動抽出
- 印刷（ブラウザ印刷でPDF保存可能）

## 使い方

### オンラインで使う
[https://via-nova.jp/resume-builder/](https://via-nova.jp/resume-builder/) にアクセスするだけ。インストール不要。

### ローカルで使う
```bash
# リポジトリをクローン
git clone https://github.com/tsakaki-vianova/resume-builder.git
cd resume-builder

# index.html をブラウザで開く（ダブルクリックでOK）
open index.html
```

> **注意:** Excel出力にExcelJSのCDNを使用しています。オフライン環境では出力が動作しない場合があります。

## ファイル構成

```
resume-builder/
├── index.html          # Webアプリ本体（スタンドアロン）
├── templates/
│   ├── 履歴書テンプレート.xlsx      # Excel出力のベーステンプレート
│   ├── 職務経歴書テンプレート.xlsx  # Excel出力のベーステンプレート
│   ├── 履歴書サンプル.xlsx          # 出力サンプル（参考）
│   └── 職務経歴書サンプル.xlsx      # 出力サンプル（参考）
└── README.md
```

## 使用ライブラリ（CDN）

| ライブラリ | バージョン | 用途 |
|-----------|-----------|------|
| [ExcelJS](https://github.com/exceljs/exceljs) | 4.4.0 | Excel (.xlsx) 生成 |
| [PDF.js](https://mozilla.github.io/pdf.js/) | 3.11.174 | PDFテキスト抽出 |
| [Mammoth.js](https://github.com/mwilliamson/mammoth.js) | 1.6.0 | Word (.docx) テキスト抽出 |

## 今後の予定

- [ ] ExcelJSによるテンプレート方式の帳票精緻化（厚生労働省様式に完全準拠）
- [ ] 写真アップロード対応
- [ ] 和暦/西暦切替UI
- [ ] 複数書類セットの管理（応募先ごとの複製）
- [ ] Next.js版への移行（サーバーサイドExcel生成）

## ライセンス

MIT

## 作者

via nova — [https://via-nova.jp](https://via-nova.jp)
