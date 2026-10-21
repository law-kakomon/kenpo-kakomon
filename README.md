# 憲法過去問帳

ロースクール既修者入試（憲法）の過去問を、**憲法の単元ごとに**引ける学習帳。

**https://law-kakomon.github.io/kenpo-kakomon/**

- **単元から引く** — 総論／人権総論／包括的基本権・平等／精神的自由／経済的自由・人身の自由／社会権・参政権／統治
- **条文から引く** — 検索欄に `21` と入れると、21条が論じられている回が並ぶ
- **論点・判例で探す** — 「政教分離」「最大判昭和50年9月10日」などで検索
- **問題と解説をその場で読む** — 同志社・立命館は PDF をページ内に表示。関学・慶應・中央はサーバー側の設定で埋め込めないため新しいタブで開く
- **解いた回に印をつける** — チェックはこの端末のブラウザにだけ残る

収録は京大・同志社・立命館・関学・慶應・中央の6校、計 75 回（2005〜2027年度）。
立命館は憲法と行政法を合わせた「公法」1冊で出題している。

**PDF は各大学の公式ページをそのまま開きます**（このリポジトリに複製は置いていません）。

## 使い方

上の URL をブラウザで開くだけ。スマホでは「ホーム画面に追加」するとアプリのように使える。

手元で動かすとき:

```bash
open 開く.command
```

## 更新

```bash
python3 tools/fetch_sources.py   # 各大学のページを見て新年度を拾う
python3 tools/digest.py <id>     # 新しい回の条文・判例・論点を取り出す
# → 出力を見て tools/classify.py に単元を書く
python3 tools/build_data.py      # data/kakomon.json と index.html への埋め込みを作り直す
```

## 姉妹サイト

科目の入口は **https://law-kakomon.github.io/** 。

- [民法過去問帳](https://law-kakomon.github.io/minpo-kakomon/)
- [民事訴訟法過去問帳](https://law-kakomon.github.io/minso-kakomon/)
- [会社法過去問帳](https://law-kakomon.github.io/kaisha-kakomon/)
- [行政法過去問帳](https://law-kakomon.github.io/gyosei-kakomon/)
- [刑法過去問帳](https://law-kakomon.github.io/keiho-kakomon/)
- [刑事訴訟法過去問帳](https://law-kakomon.github.io/keiso-kakomon/)
