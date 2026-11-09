# GPU描画を学ぶ

### [The_Book_of_Shaders](https://thebookofshaders.com/?lan=jp)
- gpu描画の仕組みというよりも、もっと根本的な描画物の数学的・アルゴリズム的な解説に感じた
- 描画もつまるところ、関数・プログラムなのだと改めて知り、目から鱗が落ちる思いだった、いや実態をつかんだという感触だった

### [WebGPUの基礎](https://webgpufundamentals.org/webgpu/lessons/ja/webgpu-fundamentals.html)
- GPU描画の仕組みに特化して書いてある印象、特にWebGPUの仕組みについて
- つまるところ、描画の要素は大きく分けて２つ：頂点シェーダー（Vertex Shader）、フラグメントシェーダー（Fragment Shader）
- それらをコンピュートシェーダー（Compute Shader）が実行する
- 頂点シェーダーが位置情報を担う
- フラグメントシェーダーは色を担う
- WebGPUのスキーマはこの図がわかりやすい（[WebGPUの概要図](https://webgpufundamentals.org/webgpu/lessons/resources/webgpu-draw-diagram.svg)）

### HLSLシェーダーの魔導書
-

### そのほかWEB上の情報
- [WebGLからWebGPUにステップアップしよう！](https://qiita.com/emadurandal/items/624fe7edd147d5a648b1)
- [opengl webgl 違いをわかりやすく解説する完全ガイド：中学生にも伝わるポイント3つ](https://chigai2.fromation.co.jp/archives/36098) 
