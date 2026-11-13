# Navidrome- README 下書き（Muse 作成・2026-11-12 確認分）

> ユーザーへの確認用です。GitHub へはまだ何も push していません。
> 承認・修正のうえ、`README.md` としてリポジトリに追加してください。

---

# Navidrome-

Navidrome 用のブラウザ・ツールを集めたリポジトリです。サーバー不要の単体 HTML ファイルで、ブラウザで開いて使います。

## ファイル

| ファイル | 内容 |
| --- | --- |
| `index.html` | Navidrome Smart Playlist (.nsp) Creator - Complete Edition |
| `SettingOption.html` | Navidrome 設定項目・環境変数 一覧 |

## index.html — スマートプレイリスト (.nsp) 作成ツール

Navidrome の仕様に準拠したスマートプレイリストを作るビルダーです。

- プレイリスト名・説明（comment）を入力
- ルート条件の一致ルール（すべて／いずれか）を選択
- 抽出条件ルールをネストグループ付きで組み立て
- 最大トラック数（空欄で無制限）、並び替えフィールド・並び順を指定
- 生成される `.nsp`（JSON）をプレビューで確認し、ファイルとして保存

## SettingOption.html — 設定項目リファレンス

Navidrome の設定項目を全 173 項目（通常設定 144 項目＋開発用フラグ 29 項目）まとめた日本語訳・解説付きリファレンスです。設定名・環境変数（`ND_*`）・現在値・日本語訳を一覧にしています。

## 使い方

1. 使いたい HTML ファイルをブラウザで開きます。
2. `index.html` で条件を組み立て、生成された `.nsp`（JSON）を保存します。
3. `.nsp` ファイルを、音楽ライブラリ内の任意のフォルダか、`PlaylistsPath` で指定したフォルダに置き、ライブラリスキャンを実行すると取り込まれます（`.m3u` プレイリストと同じ扱い。`AutoImportPlaylists` が `true`＝既定値であることが条件）。取り込まれたスマートプレイリストは「Auto-import」が有効になり、`.nsp` ファイルを編集して再スキャンすると内容が反映されます。なおスマートプレイリストは Navidrome では現在ベータ機能です。
4. `SettingOption.html` は設定の意味や環境変数を確認したいときに参照します。

--.html` の「現在値」がユーザーの実稼働 Navidrome から取ったものか、既定値かは不明（下書きでは断定していない）。実機の値なら、その旨を README に書くと読み手に伝わります。
- 2026-11-12 20:45 JST 追記：`.nsp` の取り込み手順は Navidrome 公式ドキュメント（https://www.navidrome.org/docs/usage/features/smart-playlists/ ）で確認して上記「使い方」に反映済み。ライブラリ内フォルダまたは `PlaylistsPath` に置いてスキャン、`AutoImportPlaylists` は既定 `true`、取り込み後は Auto-import 有効、スマートプレイリストはベータ。
