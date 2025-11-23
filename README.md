# My Tech & Life Blog

Hugo + PaperMod テーマを使用したブログです。
技術記事 (`tech`) と日常の記録 (`life`) を管理します。

## 1. 環境構築

### 前提条件
- **Git**: インストール済みであること
- **Hugo**: Extended Version が必要です

### Hugo のインストール (Windows)
PowerShell で以下を実行（Wingetを使用する場合）:
```powershell
winget install Hugo.Hugo.Extended
```
または [Releases](https://github.com/gohugoio/hugo/releases) から `hugo_extended_..._windows-amd64.zip` をダウンロードしてPATHを通してください。

### セットアップ
リポジトリをクローンした後、テーマを読み込むために以下を実行します（初回のみ）。
```bash
git submodule update --init --recursive
```

## 2. ローカルでの実行

```bash
hugo server -D
```
`http://localhost:1313/` にアクセスして確認できます。

## 3. 記事の作成

### 技術記事 (Tech)
```bash
hugo new content/tech/2024/my-new-tech-post.md
```

### 日常 (Life)
```bash
hugo new content/life/2024/my-diary.md
```

## 4. デプロイ

`main` ブランチにプッシュすると、GitHub Actions が自動的にビルドし、`gh-pages` ブランチにデプロイします。
GitHub のリポジトリ設定 (Settings > Pages) で、Source を `Deploy from a branch`、Branch を `gh-pages` / `root` に設定してください。

## 5. 数式の書き方

MathJax を有効にしているため、以下のように数式を書けます。

インライン: `$E = mc^2$`
ブロック:
$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$
