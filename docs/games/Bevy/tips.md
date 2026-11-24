# Bevyを扱う上でのこまごました留意事項

### プラグイン　([Bevy公式クイックスタート：プラグイン](https://bevy.dokyumento.jp/learn/quick-start/getting-started/plugins/))
- プラグインはAppを変更するコードのコレクション
- Bevyに貢献されず、別途リリースされたものは、サードパーティプラグイン
- Bevy公式サイトのAssetにあるものは、サードパーティ製のプラグイン
- DefaultPluginsでウィンドウが表示されるのは、ウィンドウインターフェースを定義する（ただし、ウィンドウの作成方法を実際に知っているわけではない）WindowPluginと、winitライブラリを使用してOSのネイティブウィンドウAPIを使用してウィンドウを作成する[WinitPlugin]があるため。

---

### wslでBevyがgpuを使用しない
> [!TIP]
> -> windows環境での開発がbetter   
> -> 以下の解決策があった。しかし、vulkanやmesaなどの中継が複数あって、パフォーマンスやメモリなどにデメリットが生じる (wsl GPU renderer [^1])
> ~~~rust
>            .set(RenderPlugin {
>                render_creation: RenderCreation::Automatic(Box::new(
>                    WgpuSettings {
>                        instance_flags: InstanceFlags::ALLOW_UNDERLYING_NONCOMPLIANT_ADAPTER,
>                        ..default()
>                    },
>                )),
>                ..default()
>            }),
> ~~~
> [^1]: https://github.com/bevyengine/bevy/discussions/22851

---

### dual MIT/Apache-2.0 license
- [Relicense Bevy under dual MIT/Apache-2.0](https://github.com/bevyengine/bevy/issues/2373)
- Apache-2.0はNOTICEファイルがあれば、その参照か保持が必要[^2]
> [^2]:https://qiita.com/byoo-myoo/items/7844ef2282e29dd194f6
- Apache-2.0は特許トロールからの防御がある程度確保される

---

### Bevyのクレート
- 含めるクレートはできるだけ小さくする
- [Bevyのクレート](https://github.com/bevyengine/bevy/blob/main/docs/cargo_features.md)からできるだけ小さいものだけを選ぶ

---

### リソース
- init_resourceで初期化
- insert_resourceで追加・上書きできる
- init_resource, insert_resourceはAppインスタンスが立ち上がったときに読み込まれるので、記述の順番通りでない。これはそれを気にしなくてよいし、気にする必要があるならそれぞれを明確に分ける必要がある。
