---
layout: post
categories: Others
author: Logan Wei
---

The table-of-contents is the first functionality I want to add to my blog.<br>
There're a lot of Jekyll plugins to support this.<br>
The one I'm using is [jekyll-toc](https://github.com/toshimaru/jekyll-toc)

However, I encountered a lot of issues during enabling this plugin.
# Doesn't work on GitHub Pages
It's because this plugin is not supported by GitHub Pages.<br>
To solve this, we need to involve GitHub Action.<br>
[https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow)

# The process '/opt/hostedtoolcache/Ruby/3.1.4/x64/bin/bundle' failed with exit code 16

You may encounter this issue with the config file GitHub recommended.<br>
The solution is to update the file Gmefile.lock.
```shell
bundle lock --add-platform x86_64-linux
```

# No repo name found. Specify using PAGES_REPO_NWO environment variables
Solution: [https://talk.jekyllrb.com/t/error-your-site-could-not-be-built-no-repo-name-found/5688](https://talk.jekyllrb.com/t/error-your-site-could-not-be-built-no-repo-name-found/5688)

# Reference
[How To Add A Table Of Contents To Jekyll Blog Posts](https://heymichellemac.com/table-of-contents-jekyll)<br>
[https://jekyllrb.com/docs/continuous-integration/github-actions/](https://talk.jekyllrb.com/t/error-your-site-could-not-be-built-no-repo-name-found/5688)<br>
[https://stackoverflow.com/questions/72331753/ruby-and-rails-github-action-exit-code-16](https://stackoverflow.com/questions/72331753/ruby-and-rails-github-action-exit-code-16)
