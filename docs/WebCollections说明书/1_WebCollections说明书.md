本文介绍 Web Collections 的一种布置方法,即布置到一个 GitHub 存储库的 Pages,但这并不是唯一的布置方法.

所用的工具是一个特定版本的 [Lore Web Collections Bin](https://crates.io/crates/lore-web-collections-bin-lexer-2026-04-07-1-impl-2026-04-07-2), 参考 [安装工具](./2_安装工具.md) 以安装.

在 GitHub 创建一个新的存储库.
在存储库的工作区创建 `Lore.toml` 后,填写以下内容:

```toml
link_base = [todo]
css_url = [todo]
from_lore_path = [todo]
to_html_path = [todo]
```

`link_base` 建议填写为 `"https://[your name].github.io/[respository name]/index"`

`css_url` 可以用默认值 `"https://fleetinglore.github.io/css/style.css"`

`from_lore_path` 建议填写为 `"lore_src"`

`to_html_path` 建议填写为 `"index"`

根据 `from_lore_path` 的值,创建文件夹 `lore_src/`, 在其中存放源文件.

执行指令

```bash
lore-web-collections-bin-lexer-2026-04-07-1-impl-2026-04-07-2
```

文件将生成至 `index/`.

启用 Pages 后可以在 `"https://[your name].github.io/[respository name]/index/xxx"` 访问 `"lore_src/xxx.lore"` 所生成的网页.

因为项目尚处于早期阶段,基本设计尚未稳定,所以就不写详细的基本设计说明了.

可以参考 [示例项目](./3_示例项目.md).
