---
public: true
---
# andrewlb "digital garden"
Public version of a digital garden.
I tried a version of this earlier in 2023 via the obsidian-garden plugin. 
I've basically tried a few different structures and theories around my blog since. At the inception of this project, it's a very traditional "portolio" style blog which I'm frankly unhappy with.

With the relaunch of my newsletter, after a few initial essays I'm already unhappy with it. Its modeled after doing the draft in obsidian, then using rsync to copy key assets over to the git repo, and deploy from there. Its not great, though its pretty fast.

What I like about it is:
- Obsidian is the editor
- Obsidian is the storage mechanism
- It's all markdown
- It's a response to past experience getting info "caught" on a CMS
- Build on astro which has a nice schema-based content model.

What I dislike:
- The rsync structure is irritating
- Feels like I'm doing more infra than writing
- Astro which is fine, but I prefer nextjs

## The idea with this
This repo is meant to be imported as a submodule into my main repo. Appropriate content buckets will be rendered in the appropriate place.
