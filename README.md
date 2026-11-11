# estechfy 公開情報ポータル（public）

Estechfy合同会社（estechfy）の各プロダクト・プロジェクトにおける公開情報（ホームページ、プライバシーポリシー、利用規約、アカウント・データ削除案内、公開用素材など）を一元管理するリポジトリです。GitHub Pages により `main` ブランチのルートから配信されます。

- **リポジトリ**: `https://github.com/estechfy/public`
- **GitHub Pages 公開トップ**: `https://estechfy.github.io/public/`

---

## ディレクトリ構成（プロジェクト単位）

全社共通のポータルをルートに配置し、各プロジェクトを独立したディレクトリで管理しています。

```text
public/
├── .nojekyll
├── README.md                  # 本ドキュメント
├── index.html                 # 会社共通公開情報ポータル（トップ）
├── assets/                    # 会社共通アセット
│   └── site.css
├── apps/                      # 互換リダイレクト用（トップページへ遷移）
│   └── index.html
├── fastplayer/                # FastPlayer（Mac向け動画再生・字幕学習・動画保護）
│   ├── index.html             # FastPlayer 公式紹介 & サポート案内 (#support)
│   ├── privacy/
│   │   └── index.html         # FastPlayer プライバシーポリシー
│   ├── terms/
│   │   └── index.html         # FastPlayer 利用規約
│   └── assets/
│       ├── fastplayer-logo.png
│       ├── protected-video-icon.png
│       └── site.css
├── dareka/                    # Dareka（名刺管理・着信表示・プライベート電話帳: com.estechfy.dareka）
│   ├── index.html             # Dareka ホーム & サポート (#support)
│   ├── privacy/
│   │   └── index.html         # Dareka プライバシーポリシー
│   ├── terms/
│   │   └── index.html         # Dareka 利用規約
│   ├── delete-account/
│   │   └── index.html         # Dareka アカウント・データ削除手順
│   └── assets/
│       ├── dareka-logo.png
│       └── site.css
└── bg/                        # Bg（BgRec：バックグラウンド録画・録音アプリ）
    ├── index.html             # Bg プライバシーポリシー
    └── privacy/
        └── index.html         # Bg プライバシーポリシー（プロジェクトURL）
```

---

## 公開URL一覧（GitHub Pages）

| プロジェクト | 用途 | 公開URL |
| :--- | :--- | :--- |
| **全社共通** | **estechfy 公開ポータル（トップ）** | **`https://estechfy.github.io/public/`** |
| **FastPlayer** | 公式ホームページ & サポート | `https://estechfy.github.io/public/fastplayer/` |
| **FastPlayer** | サポート窓口アンカー | `https://estechfy.github.io/public/fastplayer/#support` |
| **FastPlayer** | プライバシーポリシー | `https://estechfy.github.io/public/fastplayer/privacy/` |
| **FastPlayer** | 利用規約 | `https://estechfy.github.io/public/fastplayer/terms/` |
| **FastPlayer** | ロゴPNG（512×512） | `https://estechfy.github.io/public/fastplayer/assets/fastplayer-logo.png` |
| **FastPlayer** | 保護動画アイコンPNG | `https://estechfy.github.io/public/fastplayer/assets/protected-video-icon.png` |
| **Dareka** | 公式ホームページ & サポート | `https://estechfy.github.io/public/dareka/` |
| **Dareka** | プライバシーポリシー | `https://estechfy.github.io/public/dareka/privacy/` |
| **Dareka** | 利用規約 | `https://estechfy.github.io/public/dareka/terms/` |
| **Dareka** | アカウント・データ削除案内 | `https://estechfy.github.io/public/dareka/delete-account/` |
| **Dareka** | ロゴPNG（512×512） | `https://estechfy.github.io/public/dareka/assets/dareka-logo.png` |
| **Bg (BgRec)** | プライバシーポリシー | `https://estechfy.github.io/public/bg/privacy/` （`https://estechfy.github.io/public/bg/`） |

---

## 管理方針

- **プロジェクトごとの独立性**: アプリやサービスごとの公開資料は各プロジェクトフォルダ（`fastplayer/`, `dareka/`, `bg/` 等）にまとめ、独立して更新・保守します。
- **共通トップポータル**: ルートの `index.html` は estechfy の共通トップとし、提供中の全プロジェクトや共通ポリシーへのポータルとして機能します。
- **データプライバシーの明記**:
  - FastPlayer では動画本体を外部送信せず、動画暗号化鍵と識別情報のみを本人の Google Drive アプリ専用領域（appDataFolder）へ保存します。
  - Dareka では連絡先・名刺データを外部サーバーへ勝手に送信せず、端末内および本人のプライベートストレージで管理します。
  - BgRec では第三者広告SDKを含まず、録画・録音データはすべて端末内で完結します。
- **公開用情報のみの配置**: アプリの非公開ソースコード、OAuth クライアント秘密情報、認証トークン、暗号鍵、利用者の実データ、内部開発ログなどは一切含めません。
- **オープンソース・ライセンス情報**: オープンソース部品の配布およびライセンス再リンクキットは専用リポジトリ（例: `https://github.com/estechfy/fastplayer-compliance`）で管理・公開します。

---

## 各種ストア申請・登録時の設定値

### Mac App Store（FastPlayer）
- **ホームページ（Marketing URL）**: `https://estechfy.github.io/public/fastplayer/`
- **サポートURL（Support URL）**: `https://estechfy.github.io/public/fastplayer/#support`
- **プライバシーポリシーURL**: `https://estechfy.github.io/public/fastplayer/privacy/`

### Google OAuth / Google Cloud Console（FastPlayer 動画保護機能）
- **アプリケーション ホームページ**: `https://estechfy.github.io/public/fastplayer/`
- **アプリケーション プライバシー ポリシー**: `https://estechfy.github.io/public/fastplayer/privacy/`
- **アプリケーション 利用規約**: `https://estechfy.github.io/public/fastplayer/terms/`
- **ロゴ**: `fastplayer/assets/fastplayer-logo.png`（512×512px、PNG、1MB未満）

---

お問い合わせ：<support@estechfy.com>
