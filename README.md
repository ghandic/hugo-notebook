# Hugo notebook

> Hugo notebook shortcode: For rendering remote notebooks in your Hugo site

You can see this in action [on my blog](https://andrewchallis.co.uk/articles/building-a-notebook-shortcode-for-hugo/).

## Installation

### Via `git` submodules as theme components

**First ensure you are using git to version your site using `git init`**

Install this as a submodule via `git submodule add https://github.com/ghandic/hugo-notebook.git themes/hugo-notebook` and change your `config.toml`

```toml
# From (substitute your theme name)
theme = "hugo-coder"
# To
theme = ["hugo-notebook", "hugo-coder"]
```

To later update (all) submodules, use `git submodule update --rebase --remote`

### Via Hugo modules

If you're going the Hugo module route, add to your `config.toml`

```toml
[module]
  [[module.imports]]
    path = "github.com/ghandic/hugo-notebook"
```

## Included shortcodes

### `notebook`

To render remote notebooks stored on github

Usage:

```html
{{< notebook url="https://github.com/python-visualization/folium/blob/master/examples/CheckZorder.ipynb" >}}
```

Which produces:

![Imgur Hugo Notebook](https://i.imgur.com/kb3QFSP.png)
