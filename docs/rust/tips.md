# rustを扱う上でのこまごま

### Rust-GlancerをLSPとして使用
- Rust-Analyzerは標準的なLSPだけれど、メモリ消費や逐次的なチェック、リアルタイムのデバッグが重かった
- メモリ効率に特化したLSPであるRust-Glancerに切り替えた。リアルタイム性はないが、むしろそれが軽快で、実装中に警告が出ないのも逆に気が散らなくて、自分には合っていた。
- https://rust-glancer.github.io/
