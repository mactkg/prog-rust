- 資料: https://bevyengine.org/learn/book/getting-started/

## 学び

- cargo intro
- struct(def, impl)
- mut
- bevy
  - Entity: unique な int を持つタイプ
    - ID, Entity といったところ?
  - Component: `Component` trait がついている struct
    - ここに Entity のデータや振る舞いが表現されそうな感じするなー
  - System: Rust の function
    - 毎クロック呼ばれ続けてそう
    - いい感じに query できる
  - C と S はめちゃめちゃ細かく分けていったほうが良い、Person と Name は分けちゃった方がいい
    - なぜなら Name は Person 以外も持つから
  - `commands.spawn` で `()` に包んであげると Component を誕生できる
  - Time と Timer の使い方

## はまったこと

- `mut` つけ忘れて `ResMut` の `timer` が使えなかった

## 知りたいこと、疑問に思ったこと

- ファイル分割のやり方
- struct
  - pub って何
- trait
- `commands.spawn` でやってる `()` って何をしているのか
  - `()`の中で一緒に定義したコンポーネントは同じエンティティになっているのか？
- `add_system` すると一体何が起こっているのか（いい感じに引数にアイテムが渡る仕組みも摩訶不思議）
- `&str` と `String` の違い
