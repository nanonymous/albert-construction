See `gh-pages` branch for the website code. You're meant to work only in that branch.

Installation
============

Install [Ruby](http://rubyinstaller.org/downloads/)

`gem install jekyll`

```
git clone [this repo git url]
cd [this repo folder]
git checkout gh-pages
```

Running
=======

`jekyll serve --baseurl ''`

Then go to http://localhost:4000 and you should see the website.

When you edit your code save it and refresh the webpage - it should display your changes. 

(only changes to `_config.yml` aren't hot reloaded and require stopping and starting jekyll process again)