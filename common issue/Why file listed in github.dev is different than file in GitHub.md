# Why file listed in github.dev is different than file in GitHub
## Answer
File listed in `github.dev` might be different than file in GitHub, even if one reloads `github.dev` web page.

The reason why it occurs is that

+ When one tries to reload web page, the web browser will fetch data on web browser's cache (if it exists).
+ On the other hand, when one has perform some operation (especially with git command) on the branch (called `master`) of specific repo (called `CSharp`), such as

  - push to `master` branch from local repo as source
  - force push to `master` branch from local repo as source
  - merge from other branch into `master` branch.

it will update data into server but NOT browser cache.

Thus, when one reloads `github.dev` web page, it will fetch data on web browser's cache (which is old and different than the data in server).

## Solution
How to solve it?

Since, when one tries to reload web page, the web browser will fetch data on web browser's cache (if it exists),

one can hard refresh to bypass fetching data on web browser's cache and will fetch data from server.

## reference
### Google Gemini
From [Google Gemini's reponse](https://g.co/gemini/share/db9bfbd8edbe) of this question -- When file listed in Github is NOT same file listed in github.dev after force-pushing?
