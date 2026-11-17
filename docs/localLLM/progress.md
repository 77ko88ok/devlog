# local LLMを用いた試行錯誤の記録

## LM StudioとOpenCodeの連携

### OpenCode
- V1, V2があり、設定ファイルのjsonに互換性がない
- 2025年の情報はv1が主体で、現在はあまり参考にならない。AIの情報も同等なので、逐次的にドキュメントを参照する必要がある。

### MCP, Plugins
- context-mode: コンテクスト長の節約効果はあまり実感できなかった。それよりもサブエージェントに切り替えるほうが確実そう
- claude-mem: 同じ作業を試行錯誤していると、その記録も残ってしまって、逆にその確認作業で時間とコンテクストをたくさん使用することになった。削除した
- Agent-Memory: セッション間の情報は共有して、はじめましてからスタートするのを避ける。マークダウンで何が記録されているか確認しやすいのもよい。しばらく使用してみる。

## models
### Gemini API
- [利用規約](https://aistudio.google.com/docs/terms?hl=ja)
- [料金表と利用範囲と学習使用範囲](https://aistudio.google.com/docs/pricing?hl=ja)

### Gemma-4
- Gemma-4-12b-qat
- Gemma-4-e4b-qat
- Gemma-4-e2b-qat
- 
