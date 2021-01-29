---
description: Versioning can be maintained through variant manipulation by the author.
---

# Versioning

Versioning with GitBook can be done using variants but can become confusing unless the default behavior that GitBok uses for GitHub integrations is considered. The following rules are implemented by GitBook by default. They can be changed by changing the **slug** of the variant.

* The initial variant points to the master branch.
* Author created variants will use the variant slug as the branch name and the variant is merged to the branch.
* Changing the variant slug after a variant has been merged to the repo will create a new branch and merge the variant to it leaving the old branch intact.

It is important to never merge any one branch to another in GitHub as merged content from one variant could overwrite another's. This will result in versions showing content from other versions.

### Using Semantic Versioning

Consider a simple use case of semantic versioning

1. **MAJOR** version when making incompatible API changes,
2. **MINOR** version when adding functionality in a backward compatible manner, and
3. **PATCH** version when making backward compatible bug fixes.

Using semantic versioning milestones \(_major, minor, and patch_\) can be an issue if the content is not prepared. Each would need a new variant and variants currently become visible to customers as soon as they are created. Unless the content is ready, customers will see nothing but a copy of old content.

{% hint style="info" %}
As mentioned in the section **Variants**: 

A ticket has been submitted to GitBook to determine if a variant can be hidden independently of other variants.
{% endhint %}

If GitBook commits to adding hiding variants, then versioning using variants become easy.    

### Solution \#1

Separate repos could be used based on semantic **major** releases \(v1, v2, etc.\).

| Version | GitHub Repo | GitBook Space |
| :--- | :--- | :--- |
| v1 | owner/gitbook-v1 | gitbook-v1 |
| v2 | owner/gitbook-v2 | gitbook-v2 |

Here **minor** and **patch** releases could be added as variants. However, the content must be available or the customer will not see a true picture. If GitBook allows hiding of variants then unprepared content would not be an issue.

* 1.0.1
* 1.0.2
* 1.1.0

### Solution \#2

Use separate repos as in **Solution \#1** but never create a new variant. Version 1 would simply be a constant work in progress. This could be limiting if documentation must follow product semantic versioning.   

### Solutions \#3

If GitBook adds hidden variants then all releases could exist in one GitBook space and GitHub repo.

| Version | GitHub Repo | GitBook Space |
| :--- | :--- | :--- |
| v1.0.0 | owner/gitbook-v1.0.0 | gitbook-v1.0.0 |
| v1.0.0 | owner/gitbook-v1.0.1 | gitbook-v1.0.1 |
| v1.1.0 | owner/gitbook-v1.1.0 | gitbook-v1.1.0 |
| v2.0.0 | owner/gitbook-v2.0.0 | gitbook-v2.0.0 |

### Solution \#4

Do not use the GitHub integration feature from GitBook. GitBook stores content in the Google Cloud. While the data can be exported this is a dependency on a third party. It may be hard to format the data back to GitHub.









