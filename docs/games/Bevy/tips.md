# Bevyを扱う上でのこまごました留意事項

### プラグイン　([Bevy公式クイックスタート：プラグイン](https://bevy.dokyumento.jp/learn/quick-start/getting-started/plugins/))
- プラグインはAppを変更するコードのコレクション
- Bevyに貢献されず、別途リリースされたものは、サードパーティプラグイン
- Bevy公式サイトのAssetにあるものは、サードパーティ製のプラグイン
- DefaultPluginsでウィンドウが表示されるのは、ウィンドウインターフェースを定義する（ただし、ウィンドウの作成方法を実際に知っているわけではない）WindowPluginと、winitライブラリを使用してOSのネイティブウィンドウAPIを使用してウィンドウを作成する[WinitPlugin]があるため。

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
