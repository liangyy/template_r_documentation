# template_r_documentation

This is a light template for documentation based on rmarkdown.

## Overview

This is based on rmarkdown. As a quick look at how things work, the way the documentations glued together is:

1. `_site.yml` tells what should be at navigation bar and it also determines the overall style.
2. `index.html` and other files that are linked by `_site.yml` can further link to other files (namely sub contents).
3. run `render_site([file-name])` to generate `html` file from `Rmd` file.
4. add, commit, and push everything at the end of the day.

## Notes

1. `docs/` contains all `html` files and be sure to enable Github Pages (`docs/` mode).
2. put all `Rmd` files at `rmd/` and in R terminal, run `render_site('rmd/filename.Rmd')` and it will generate the corresponding `html` at `docs/`

## Build yourself

All you need to get started is the files in `rmd/`. Once you get them, do the following in R terminal:

```
setwd('some_path/template_r_documentation')
library(rmarkdown)
render_site(input = 'rmd/')
```

To render a new file, say `new.Rmd`, do:

```
render_site(input = 'rmd/new.Rmd`)
```

## See also

This is a super light and lazy (quick) solution. It is inspired by [this post](http://nickstrayer.me/RMarkdown_Sites_tutorial/) and [workflowr](https://github.com/jdblischak/workflowr). To get a more advanced and prettier solution, please check out [workflowr](https://github.com/jdblischak/workflowr).
