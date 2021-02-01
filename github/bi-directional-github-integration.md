---
description: Syncing a space in either direction.
---

# Bi-directional GitHub integration

Integrating GitBook with GitHub can provide changes made outside of the GitBook online editor to sync back to GitBook. This can be problematic if changes made to the repo by other tools end up overwriting the GitBook saved \(not merged\) image.

When using the online editor it may be best to have GitHub contributors push to a repo branch that is not integrated. Then let the author figure out the merge to a branch \(variant\).

Because the online editor saves many changes as a single draft, merges must send the entire draft to the repo. This makes it difficult to provide detailed commit messages about each page change unless every page change is isolated from other work and then merged before working on another page. This is difficult to do. 

