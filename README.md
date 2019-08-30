
# tab

so I made one of these before and it was pretty cool, but I realised pretty quickly that it had some serious privacy implications due to the fact that it:

+ needed to be hosted to work properly (*very* unique query)
+ queried google for its fonts (unique, but a very common internet-wide request)
+ queried github gists for config data (*very* unique query again)

these things repeated over and over every time you open a new tab make you pretty identifiable.  so, in the interests of *not* doing that, because we've learned from our past stupidity, this new new tab is entirely serverless and local to the machine it's being run on.

this new tab is entirely contained in one file (minus an optional font file) and has no external configuration.  this has the added benefit of making it *gotdang fast*.

the red number in the top right corner is a [weird date](https://github.com/qxoko/WeirdDate).

## usage

it's pretty darn simple.  point your browser's new tab/homepage to `index.html`.  optionally, you can point the `@font-face` url to a specific font file.

then, you type a command, which is generally a single character, followed by a space and your search query.

for instance, `a product name` will search `amazon` for `product name`.  simply typing `a` and hitting enter will take you to the homepage.

## commands

```
// main
g    <query>   — google
img  <query>   — google images
m              — mail.protonmail.com
todo <tag>     — workflowy + jump to tag

// chat
d              — discord web
s <workspace>  — slack

// social
tw <query>     — twitter
r  <subreddit> — reddit
t  <blog name> — tumblr

// entertainment
y  <query>     — youtube.com + "s" for sub box
n  <query>     — netflix

// other
a    <query>   — amazon.co.uk
w    <query>   — wikipedia
git  <query>   — github.com
dict <query>   — dictionary.com
thes <query>   — thesaurus.com

// utility
x <url>        — force redirect if the box fails to treat a pasted url correctly
```