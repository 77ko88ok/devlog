# Bevyを扱う上でのこまごました留意事項

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
