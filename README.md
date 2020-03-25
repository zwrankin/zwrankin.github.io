# Minimal Mistakes remote theme starter
Repo for my personal website http://zwrankin.github.io/.  
 Hosted on [GitHub Pages](https://pages.github.com/) | Built using [Jekyll](https://jekyllrb.com/) | Theme by [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes). 


## Usage
To serve locally, navigate to the directory root and run `bundle exec jekyll serve`, with the optional `--incremental` flag.  
You could also manually run `bundle` to update, then `jekyll serve`. 


## Installation
See https://jekyllrb.com/docs/installation/  
Installing rub/gem/bunlder without sudo can be a pain. I installed it on Mac with Homebrew, following the helpful instructions here: https://jekyllrb.com/docs/troubleshooting/#no-sudo, then  
```
brew install ruby
gem install bundler
gem install jekyl
```

## Customization
There are various ways to customize. Basic configurations are handled in the `_config.yml`.  (https://mmistakes.github.io/minimal-mistakes/docs/overriding-theme-defaults/). However, there are additional customizations that can be handled at various levels.  
To customize `layouts` or `includes`, download the versions from https://github.com/mmistakes/minimal-mistakes, then make local edits (which will override the previous versions from the gem).  
To customize css, you must download the entire contents of https://github.com/mmistakes/minimal-mistakes/tree/master/_sass.  
**Notes to self**  
- The first (and as of 3/20/2020, only) css customization is the `_archive.scss` layout, in which I updated the width of feature rows so that the blog post previews don't overrun when using `classes: wide` in the frontmatter of `home.html` layout. 
- All external links open in new tabs as per [this script](https://github.com/gernotstarke/minimal-mistakes/commit/9ba387bbe3160e83f54c7f63f303254155f9fab5)
- Here are the [custom favicon instructions](https://github.com/mmistakes/minimal-mistakes/issues/949)
- For my resume, there's no first-class support from minimal mistakes theme to do so [issue](https://github.com/mmistakes/minimal-mistakes/issues/323). There are third party embedding plugins but I'd rather just use the current external link (to the source of this PDF file)

## Upgrading
Currently minimal mistakes tracks the latest version on the remote master branch.  The built site source include `Minimal Mistakes Jekyll Theme 4.19.1 by Michael Rose` at the top of every `.html` file. If needed, you can pin an old version of `remote_theme: mmistakes/minimal-mistakes` within `_config.yml`.  For more, see https://mmistakes.github.io/minimal-mistakes/docs/upgrading/.  
Note that my repo is not forked from https://github.com/mmistakes/minimal-mistakes, so upgrading could be a fairly manual process of comparing my customized files to the remote repo. Unclear how frequently I'd need to upgrade. Perhaps in the future I'd add a remote head. 


## Troubleshooting
First, make sure dependencies are cleared by running `bundle update`.  
Second, try pinning an old version of `remote_theme: mmistakes/minimal-mistakes` within `_config.yml` as per above. 


## Helpful Resources:
- https://pages.github.com/ 
- https://help.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll
- https://jekyllrb.com/docs/
- https://jekyllrb.com/docs/github-pages/
- https://jekyllrb.com/docs/step-by-step/01-setup/
- https://github.com/mmistakes/minimal-mistakes 
- https://github.com/mmistakes/mm-github-pages-starter
- https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
- https://mmistakes.github.io/minimal-mistakes/docs/overriding-theme-defaults/  


## Attribution 
Some images courtesy of https://thenounproject.com/  
- Brain: Sergey Patutin
