# Minimal Mistakes remote theme starter
Repo for my personal website http://zwrankin.github.io/.  
 Hosted on [GitHub Pages](https://pages.github.com/) | Built using [Jekyll](https://jekyllrb.com/) | Theme by [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes). 

## Usage
To serve locally, navigate to the directory root and run `bundle exec jekyll serve`.  
You could also manually run `bundle` to update, then `jekyll serve`. 

## Resources:
- https://pages.github.com/ 
- https://help.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll
- https://jekyllrb.com/docs/
- https://jekyllrb.com/docs/github-pages/
- https://jekyllrb.com/docs/step-by-step/01-setup/
- https://github.com/mmistakes/minimal-mistakes 
- https://github.com/mmistakes/mm-github-pages-starter
- https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
- https://mmistakes.github.io/minimal-mistakes/docs/overriding-theme-defaults/  

## Installation
See https://jekyllrb.com/docs/installation/  
Installing rub/gem/bunlder without sudo can be a pain. I installed it on Mac with Homebrew, following the helpful instructions here: https://jekyllrb.com/docs/troubleshooting/#no-sudo, then  
```
brew install ruby
gem install bundler
gem install jekyl
```

## Troubleshooting
First, make sure dependencies are cleared by running `bundle update`.  
Second, try pinning an old version of `remote_theme: mmistakes/minimal-mistakes` within `_config.yml`. Currently it tracks the latest version on the remote master branch.  The built site source include `Minimal Mistakes Jekyll Theme 4.19.1 by Michael Rose` at the top of every `.html` file. For more, see https://mmistakes.github.io/minimal-mistakes/docs/upgrading/

## Attribution 
Some images courtesy of https://thenounproject.com/  
- Brain: Sergey Patutin
