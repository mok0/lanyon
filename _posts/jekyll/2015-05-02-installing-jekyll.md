---
layout: post
title:  "Installing Jekyll"
date:   2015-05-02 20:56:12
category: jekyll
---

If you are using Python 3 as a standard, the [Jekyll] installation
from [homebrew] might give you problems, because the Jekyll
installation out-of-the box uses the syntax higlighter [Pygments],
which does not work under Python 3. This is the rather mysterious
error I got:

{% highlight shell %}
$ jekyll serve --trace
Configuration file: /Users/mok/github/mok0.github.io/_config.yml
            Source: /Users/mok/github/mok0.github.io
       Destination: /Users/mok/github/mok0.github.io/_site
      Generating...
  Liquid Exception: No header received back. in _posts/2015-05-02-welcome-to-jekyll.markdown
{% endhighlight %}

Instead, use the Ruby highlighter `rouge`. In _config.yml, add:

    highlighter: rouge

and install the rouge highlighter gem:

    gem install rouge

Now the installation should go without problems.

[homebrew]: http://brew.sh
[jekyll]: http://jekyllrb.com
[pygments]: http://pygments.org
