# Daily Log

### 2026.11.19
- AIオーケストレーション時のセキュリティMCPを考案した([defender_for_subagents](localLLM/defender_for_subagents.md))
- OpenCodeでのオーケストレーション設定を学んだ

### 2026.11.18
- AIオーケストレーションを行う際のセキュリティについて学んだ
- bevyのECSを、公式quick startで学んだ
- RustでのMCPサーバーの構築方法を学習始めた
- Burnの計算バックエンドについて学び、新たなクレートの開発を検討した

### 2026.11.17
- OpenCodeとLM Studioとの連携などを学んだ

### 2926.11.16
- wgslを学んだ group, binding

### 2026.11.15
- local LLMを用いてOpenCodeで作業してみたが、コンテクスト長に悩まされた
- primary-Agent, sub-Agentにしてみた
- bevyでの当たり判定にはrapierを使ってみる
- bevyでの三人称カメラプラグインをみつけたので使ってみる

### 2026.11.14
- local LLMを用いる際にマルチGPUができないか検証した
- rtx3060とgt1030はすでにドライバーに互換性がなくなっていたので、互換性のある過去のドライバーにロールバックするか、マルチGPUをあきらめるかの二択になり、セキュリティを優先してrtx3060のみの単一GPUで動かすことにした
- 『リアルタイムグラフィックスの数学』を少し読み進めた。これが一番わかりやすいかもしれない。あるいはある程度勉強が進んだからそう感じたのかもしれない。
- Rust, Bevyの学習は少し休憩して、他の実装や日常生活の整理をすすめた
- Ready to Stop Timer Bar, mod翻訳, それぞれのrepoを作成して作業開始

### 2026.11.13
- local LLMのセッティングについて学んだ
- Rustでのデータサイエンスでの前処理用cratesを整理した

### 2026.11.12
- Burnをpython環境で使用する方法を学んだ
- Burnをjupyter notebookで実行
- KaggleのHousing PricesでBurnを試した

### 2026.11.11
- WebGPUの基礎を読み進めると突如わからない用語・文法に当たって混乱した
- 別のリソースを探す
- wgpuとwgslのちがいが少しわかった

### 2026.11.10
- wgpuとは？webGPUとの違いは？を調べた
- ゲーム開発の環境調整

### 2026.11.9
- HLSLシェーダーの魔導書を読み始めた
- 独自レンダリングの実装手順について整理した
- WebGPUの概略を知って、先行きが見えてワクワクしたが、同時にその遠い景色にぞっとした

### 2026.11.8
- Burnの資料あつめ
- The Book of Shaders　完読
- WebGPUの基礎　読み始め

### 2026.11.7
- Bevyのtipsを整理しはじめた
- rust-analyzerが重かったので、rust-glancerにしてみたら、良い感じだった
- glbを読み込んだworldで物理移動3dカメラを組み込み、動いた！[bevy_loading_glb](https://github.com/77ko88ok/bevy_loading_glb)

### 2026.11.6
- The book of shadersを読み進めた chapter6まで 
- シェーダーのuniformが少しわかった

### 2026.11.5
- glb/gltfを学んだ
- bevy公式exampleをもとに、gltf、glbを読み込んでみた
- gltfのファイル形式をみてgltfファイルとその構造を知った

### 2026.11.4
- devlog 開設
- The Book of Shadersの日本語訳を読み進め始めた
- https://github.com/patriciogonzalezvivo/thebookofshaders/blob/master/README-jp.md
