# rustを扱う上でのこまごま

### Rust-GlancerをLSPとして使用
- Rust-Analyzerは標準的なLSPだけれど、メモリ消費や逐次的なチェック、リアルタイムのデバッグが重かった
- メモリ効率に特化したLSPであるRust-Glancerに切り替えた。リアルタイム性はないが、むしろそれが軽快で、実装中に警告が出ないのも逆に気が散らなくて、自分には合っていた。
- https://rust-glancer.github.io/

### derive付与の挙動
- #[derive(...)] は 1つの型（struct, enum, union）に対して適用する属性なので、複数の型を一度に指定することはできない。つまり、 「複数の struct をまとめて derive する」はできない。
- 複数の struct に同じ derive を適用する場合は、マクロを使うが、よっぽどたくさんの型を作成するのでなければ手書きが早い気がする。
```rust
Rustmacro_rules! define_struct {
    ($name:ident) => {
        #[derive(Debug, Clone)]
        struct $name {
            value: i32,
        }
    };
}

define_struct!(Foo);
define_struct!(Bar);
```

### RON
- JSON(JavaScript Object Notation)ではない、[Rusty Object Notation](https://github.com/ron-rs/ron)
- RUSTの記法を模した記述ができる、末カンマが許される、コメントアウトが許される
- `[dependencies] ron=??`が必要
