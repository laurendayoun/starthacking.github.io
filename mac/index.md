---
layout: page
title: Mac
---

# First Steps

Before doing any serious hacking, you should install the Command Line Tools for
Xcode and Homebrew. The CLI tools contain utilities and compilers such as make,
gcc, git, and so on. [Homebrew][brew] is a package manager for Mac OS X that
makes it really easy to install stuff.

How to install the command line tools depends on the version of OS X that you
are running. The following method should work in most cases: open up Terminal,
run `xcode-select --install`, and follow the prompts to install the command
line tools.

Installing [Homebrew][brew] is really easy. Copy and paste the following string
into a Terminal prompt, and press enter.

```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Afterwards, make sure to add the Homebrew binary path to your `$PATH`. You can
do this by appending the following line to your `.bashrc` (or equivalent for
your shell):

```bash
export PATH=/usr/local/bin:$PATH
```

# Getting Started with [x]

{% for post in site.posts %}
    {% if post.categories contains 'mac' %}
* [{{ post.title }}]({{ post.url }})
    {% endif %}
{% endfor %}

[brew]: http://brew.sh/
