# Rustを学ぶ

### 細かい記法の話
- Rustにおける :: は パス　[Paths](https://doc.rust-lang.org/reference/paths.html)
- パスは、アイテム・値・タイプ・マクロ・属性の参照に用いる
- Rustにおける . は　メソッドの参照か呼び出し [Methods](https://doc.rust-lang.org/book/ch05-03-method-syntax.html)

### modとuse　[The book モジュールを定義して、スコープとプライバシーを制御する](https://doc.rust-jp.rs/book-ja/ch07-02-defining-modules-to-control-scope-and-privacy.html)
- modはモジュールを登録する。登録したモジュール内のコードを使用可能にする（コンパイラが読み取れるようにする）
- 階層が深い場合には、ディレクトリ名と同名の.rsが必要で、その.rsに下層のモジュールを(pub) modで登録する (よく読むと、the bookにそうでないとは書かれていない)
- useは登録したモジュール内や他のモジュール内のコードへのショートカット（または、シンボリックリンク）を作る
- 自作モジュールのコードを他のモジュールやクレートルートで使用する場合には、該当コードの公開（pubをつける）を忘れずに
- lib.rsは、そのクレート内で使用するクレートをインポートできる。再公開するモジュールにpubをつけ、main.rsでuse プロジェクトクレート名::*;で使用できる

### 未整理
- wgpuは、webGPU APIを基にした？、Rustのcrate？で、Rustでgpuを使用する手段の一つ（[wgpu(Rust)入門|wgpu30で動く三角関数](https://www.issoh.co.jp/tech/details/4094/)）
- Query内のwithの挙動
- ジェネリックプラグインとは？
