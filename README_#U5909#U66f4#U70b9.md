# 2級建築士 ○×アプリ 統一版（変更点まとめ）

## やったこと
- **全アプリを ○× 形式に統一**（5択は1選択肢ずつ○×に分解）
- **共通エンジンに統一**：分野別出題・間違い復習・正答率リング・ポイント解説 が全アプリ共通
- **ファイル名をスペース無しに統一**（`科目_種別.html`）→ `%20` 問題が解消、リンク・検索が安定
- **index.html（メニュー）と search.html（横断検索）を新ファイル名で再構築**
- 誤答記録は window.storage →（無ければ）localStorage →（無ければ）メモリ の3段で安全に保存

## 形式の変換
| 元の形式 | 変換 |
|---|---|
| `a:true / a:false`（18ファイル） | そのまま統一エンジンへ |
| `a:1 / a:2`（1=○,2=×／8ファイル） | `a:true / a:false` に変換 |
| 5択（`kozo gensen.html`） | 各選択肢を○×に分解（10問→50問） |

## ファイル名 旧→新
| 旧 | 新 |
|---|---|
| keikaku quiz.html | keikaku_marathon.html |
| kozo quiz.html | kozo_marathon.html |
| sekou quiz.html | sekou_marathon.html |
| kozo gensen.html | kozo_gensen.html（5択→○×50問） |
| gensen b / b2 / d quiz.html | gensen_b.html / gensen_b2.html / gensen_d.html |
| houki kouzou quiz.html | houki_kozo.html |
| houki note quiz.html | houki_note.html |
| hisshou1 houki / kozo quiz.html | hisshou1_houki.html / hisshou1_kozo.html |
| kakunin1 houki / keikaku quiz.html | kakunin1_houki.html / kakunin1_keikaku.html |
| houki kakunin itoshima (2) quiz.html | houki_itoshima1.html / houki_itoshima2.html |
| kokai moshi2 (houki/kouzou/sekou/_) quiz.html | moshi2_keikaku/houki/kozo/sekou.html |
| moshi2-(keikaku/houki/kozo/sekou).html | moshi2b_keikaku/houki/kozo/sekou.html |

## 注意点（要確認）
1. **`moshi3 *` 4ファイルは除外しました**
   → `kokai moshi2 *` と**バイト単位で完全に同一**（中身も「公開模試②」のまま）の重複だったためです。本物の公開模試③ができたら教えてください。残したい場合も対応します。
2. **公開模試②が2セットあります**
   → `kokai moshi2 *`（→ `moshi2_*`）と `moshi2-*`（→ `moshi2b_*`）は**中身が違う別データ**でした。どちらか不要なら削除できます。
3. **5択分解の解説**
   → 「最も不適当なものはどれか」型を分解したため、誤りの選択肢には元の解説、正しい選択肢には「正しい記述。」を付けています。必要なら個別解説を追記できます。

## GitHub Pages への反映
ZIP内のファイルをリポジトリにアップロード（同名は上書き）すれば反映されます。
旧ファイル名（スペース入り）は不要になったら削除してOKです。
