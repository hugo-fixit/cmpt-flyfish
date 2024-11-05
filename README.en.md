# Fly Fish

👉 English README | [简体中文说明](/README.en.md)

A canvas implementation of a small fish swimming animation effect.

## Demo

<https://lruihao.cn>

## Requirements

- FixIt v0.3.12 or later.

## Install Component

The installation method is the same as [installing a theme](https://fixit.lruihao.cn/documentation/installation/). There are several ways to install, choose one, for example, install through Hugo Modules:

### Install as Hugo Module

First make sure that your project itself is a [Hugo module](https://gohugo.io/hugo-modules/use-modules/#initialize-a-new-module).

Then add this theme component to your `hugo.toml` configuration file:

```toml
[module]
  [[module.imports]]
    path = "github.com/hugo-fixit/FixIt"
  [[module.imports]]
    path = "github.com/hugo-fixit/cmpt-flyfish"
```

On the first start of Hugo it will download the required files.

To update to the latest version of the module run:

```bash
hugo mod get -u
hugo mod tidy
```

### Install as Git Submodule

Clone [FixIt](https://github.com/hugo-fixit) and this git repository into your theme folder and add it as submodules of your website directory.

```bash
git submodule add https://github.com/hugo-fixit/FixIt.git themes/FixIt
git submodule add https://github.com/hugo-fixit/cmpt-flyfish.git themes/cmpt-flyfish
```

Next edit `hugo.toml` of your project and add this theme component to your themes:

```toml
theme = ["FixIt", "cmpt-flyfish"]
```

## Configuration

In order to Inject the partial `cmpt-flyfish.html` into the `custom-assets` through the [custom block](https://fixit.lruihao.cn/references/blocks/) opened by the FixIt theme in the `layouts/partials/custom.html` file, you need to fill in the following necessary configurations:

```toml
[params]
  [params.customPartials]
    head = []
    profile = []
    aside = []
    comment = []
    footer = []
    widgets = []
    assets = [
      "inject/cmpt-flyfish.html",
    ]
    postFooterBefore = []
    postFooterAfter = []
```

Configuration of the Fly Fish theme color and enable animation:

```toml
[params]
  [params.flyfish]
    enable = true
    light = "rgb(0 119 190 / 10%)"
    dark = "rgb(255 255 255 / 10%)"
```

## References

- [Develop Theme Components | FixIt](https://fixit.lruihao.cn/contributing/components/)
- [How to Develop a Hugo Theme Component | FixIt](https://fixit.lruihao.cn/components/dev-component/)
