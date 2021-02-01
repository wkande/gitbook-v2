---
description: A variant is an other version of the content.
---

# Variants

[https://docs.gitbook.com/editing-content/variants](https://docs.gitbook.com/editing-content/variants)

GitBook places each variant on its own branch and as such merging branches as a traditional operation is not recommended within a GitHub Repo.

GitBook creates an initial variant upon space creation. By default, the initial variant is merged to the repo's master branch. It is hidden in GitBook until a new variant is added by an author. The new variant will be pushed to a branch in the repo using the variant's slug as the branch name. This behavior is by design but changing the behavior is possible.

Each variant is an independent copy of the content from otehr variants. A new variant is created from the currently selected variant.

Older variants can be updated without changing other variants. Useful to make corrections to older documentation. 

It should be noted that each time a variant is created it will go live \(available to users\) once the variant is merged with its GitHub repo's branch. GitBook does not allow the disabling of a variant during its development to hide it from users.

{% hint style="info" %}
A ticket has been submitted to GitBook to determine if a variant can be hidden independently of other variants.

Response 1/30/2021: The variant is hidden until the draft is first merged.  
  
Response 2/1/2021: Try restoring a merge. \(When trying this the Restore selection is disabled so it did not work\).
{% endhint %}



