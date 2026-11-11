# estechfy アプリ公開情報（プロジェクト別公開リポジトリ）

プロジェクト（アプリ）単位でホームページ、プライバシーポリシー、利用規約、アカウント・データ削除案内、公開用ロゴを管理する公開リポジトリです。GitHub Pages は `main` ブランチのルートを配信します。

## ディレクトリ構成（プロジェクト単位）

```text
public/
├── apps/                     # 全プロジェクト一覧ポータル
├── dareka/                   # Dareka（名刺管理・着信表示・プライベート電話帳: com.estechfy.dareka）
│   ├── index.html            # Dareka ホーム
│   ├── privacy/index.html    # Dareka プライバシーポリシー
│   ├── terms/index.html      # Dareka 利用規約
│   ├── delete-account/       # Dareka アカウント・データ削除手順（Google Play Data Safety 対応）
│   └── assets/               # Dareka 公開ロゴ（512×512 PNG）
├── fastplayer/               # FastPlayer（Mac向け動画再生・字幕学習・動画保護）
│   ├── index.html            # FastPlayer ホーム
│   ├── privacy/index.html    # FastPlayer プライバシーポリシー
│   ├── terms/index.html      # FastPlayer 利用規約
│   └── assets/               # FastPlayer 公開ロゴ
└── bg/                       # Bg（BgRec：録画・録音アプリ）
    └── privacy/index.html    # Bg プライバシーポリシー（ルート index.html も後方互換のため維持）
```

## 公開URL（GitHub Pages）

| プロジェクト | 用途 | URL |
| :--- | :--- | :--- |
| **全体** | 公開情報一覧 | https://estechfy.github.io/public/apps/ |
| **Dareka** | ホーム | https://estechfy.github.io/public/dareka/ |
| **Dareka** | プライバシーポリシー | https://estechfy.github.io/public/dareka/privacy/ |
| **Dareka** | 利用規約 | https://estechfy.github.io/public/dareka/terms/ |
| **Dareka** | アカウント・データ削除案内 | https://estechfy.github.io/public/dareka/delete-account/ |
| **Dareka** | ロゴPNG（512×512） | https://estechfy.github.io/public/dareka/assets/dareka-logo.png |
| **FastPlayer** | ホーム | https://estechfy.github.io/public/fastplayer/ |
| **FastPlayer** | プライバシーポリシー | https://estechfy.github.io/public/fastplayer/privacy/ |
| **FastPlayer** | 利用規約 | https://estechfy.github.io/public/fastplayer/terms/ |
| **FastPlayer** | ロゴPNG（512×512） | https://estechfy.github.io/public/fastplayer/assets/fastplayer-logo.png |
| **Bg（BgRec）** | プライバシーポリシー | https://estechfy.github.io/public/bg/privacy/ （旧URL: https://estechfy.github.io/public/ ） |

## 管理方針

- アプリごとの公開資料を専用フォルダ（`dareka/`、`fastplayer/`、`bg/`）にまとめ、既存URLとの後方互換も維持します。
- 公開してよいページと画像だけを保存します。アプリの非公開ソース、OAuthクライアント秘密情報、認証トークン、利用者のデータ、開発ログは含めません。

お問い合わせ：support@estechfy.com
