---
author: John Lecocq
title: About Reports
---

**Reports** is a blog written by John Lecocq. In it you will find formal and informal articles about sports, economics, health, politics, and more. It is written in [R](https://www.r-project.org/foundation/) using Blogdown [Yihui Xie](https://yihui.org/en/) and Hugo. The theme for this site is called XMag which is available on Github [here w/ MIT license](https://github.com/yihui/hugo-xmag).

# Purpose

What you will get from this blog is:

- A biomedical engineer's perspective on current affairs within in the US

- Data-driven analyses to help characterize the world

- Short videos, images, and figures in to help form an intuition on the issues

- References for factual statements and inclusion of relevant data

- Proposals for civil, economic and healthcare solutions

Why you should follow this blog:

- To consume quick, digestible information on various important topics

- To keep in contact with the author, John Lecocq

- To reference scholarly and authoritative sources

- Everyone else is banned

Most features can be configured through `config.toml`, and a few can be enabled by custom layouts.

# Content

By default, your site title will be displayed at the top in Blackletter fonts if your web browser and operating system support Blackletter fonts. Essentially, for every English letter `X` in your site title, it is substituted with `&Xfr;`, e.g. the Blackletter version of `A` is `&Afr;` (&Afr;). Below are the letters from A to Z:

## &Afr;&Bfr;&Cfr;&Dfr;&Efr;&Ffr;&Gfr;&Hfr;&Ifr;&Jfr;&Kfr;&Lfr;&Mfr;&Nfr;&Ofr;&Pfr;&Qfr;&Rfr;&Sfr;&Tfr;&Ufr;&Vfr;&Wfr;&Xfr;&Yfr;&Zfr;

Alternatively, you can provide a banner image:

```toml
[params.banner]
    src = "/path/to/banner.png"
    alt = "alternative text on image"
```

By default, each summary block on the homepage contains the first 200 letters extracted from all paragraphs of an article. I find Hugo's built in `.Summary` often unsatisfactory (e.g. it may contain headings and code blocks, which really should not go to the summary), so I wrote my own version. It works much better and the size of most summary blocks will be the same, unless certain articles are really short. The length 200 can be customized via `params.summary_length`.

If you are not satisfied with the automatic summary, you can specify the `description` option in the (YAML) metadata of your Markdown document, e.g.,

```yaml
title: "My Cool Post"
description: "Please use this as the summary."
```

Each summary block may contain a thumbnail, which is the first image in an article if exists. You can override it by providing the `thumbnail` option in the meta data of your Markdown document, e.g.,

```yaml
---
title: "My Cool Post"
thumbnail: "/url/of/the/image"
---
```

For each page, this theme adds an edit link to the top-right if a parameter `github_edit` is provided, so that your reader may easily help you edit a page and submit a pull request on Github.

The page footer can be defined in `.Params.footer`, and the text is treated as Markdown. Below are some sample configurations:

```toml
[params]
    summary_length = 200
    github_edit = "https://github.com/yihui/hugo-xmag/edit/master/exampleSite/content/"
    footer = "&copy; [Yihui Xie](https://yihui.org) 2017"
```

There are a few phrases that you can "translate" (I didn't use Hugo's multi-language feature just because I'm lazy):

```toml
[params.text]
    about_author = "About the Author"
    author_delimiter = ", "
    back = "Back to Home"
    edit = "Edit this page"
    tags = "Tags: "
    truncated = " &hellip;"
    uncategorized = "Uncategorized"
```

You can define a data file under `data/` to store all authors information, e.g., you can use a TOML file `data/authors.toml` (or YAML/JSON):

```
"Alice Wonder" = "I'm Alice. More about me on [my homepage](http://example.com)."
"Yihui Xie" = "Hey this is Yihui. You don't want to follow me on Twitter @xieyihui."
```

Then for an article with an author name that can be found in `data/authors.toml`, the author info will be added to the bottom of a page. For example, on this page, you can find information about me. You can change the phrase "About the Author" by changing the parameter `about_author` in `config.toml`.

To add a table of contents to an article, you can add `toc: true` to the YAML metadata of the Markdown document.

# Custom layouts

Besides the custom layout^[If this is the first time you have heard about "customizing layouts", please read the Hugo documentation first: https://gohugo.io/themes/customizing/.] files `head_custom.html` and `foot_custom.html` supported in **XMin** (see [documentation](https://xmin.yihui.org/about/)), this theme added a few more layout files such as `banner.html`, `comments.html` and `info.html` under `layouts/partials/`. The first can be used to customize the banner. The second can be used to add a comment section, e.g., if you want to use Hugo's default Disqus template, just add this to `comments.html`:

```
{{ template "_internal/disqus.html" . }}
```

You can also append arbitrary text to each article through `info.html`. For example, you may declare copyrights or briefly introduce your site.

There are other partial templates in this theme and I encourage you to read the source code to figure out what they do.

