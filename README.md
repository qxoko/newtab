
# tab

so I made one of these before and it was pretty cool, but I realised pretty quickly that it had some serious privacy implications due to the fact that it:

A) needed to be hosted to work properly (unique url)
B) queried google for its fonts (constant identical query)
C) queried github gists for config data (unique url again.  this only happened when prompted, but nevertheless).

these things repeated over and over every time you open a new tab make you pretty identifiable.  so, in the interests of *not* doing that, because we've learned from our past stupidity, this new new tab is entirely serverless and local to the machine it's being run on.

this new tab is entirely contained in one file (minus an optional font file) and has no external configuration.  this has the added benefit of making it *gotdang fast*.

## usage

it's pretty darn simple.  point your browser's new tab/homepage to `index.html`.  optionally, you can point the `@font-face` url to a specific font file.

then, you type a command, which are generally single character, followed by a space and your search query.

for instance, `a product name` will search `amazon` for `product name`.  simply typing `a` and hitting enter will take you to the homepage.

## commands

```
g <query>      — google
img <query>    — google images
a <query>      — amazon.co.uk
d              — discord web
y <query>      — youtube.com: query "s" will go to subscriptions
n <query>      — netflix
r <subreddit   — reddit
t <blog name>  — tumblr
w <query>      — wikipedia
a <query>      — amazon
git <query>    — github
dict <query>   — dictionary.com
thes <query>   — thesaurus.com
```