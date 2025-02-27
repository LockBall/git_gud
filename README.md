# git_gud
git commands and tricks

#

### clone a single folder from a repo
usefull for large repos where only a smaller portion is needed
https://stackoverflow.com/questions/600079/how-do-i-clone-a-subdirectory-only-of-a-git-repository

E.g., to clone only files in subdirectory small/ in this test repository: https://github.com/cirosantilli/test-git-partial-clone-big-small-no-bigtree  

<pre>
git clone -n --depth=1 --filter=tree:0 https://github.com/cirosantilli/test-git-partial-clone-big-small-no-bigtree
cd test-git-partial-clone-big-small-no-bigtree
git sparse-checkout set --no-cone /small
git checkout
</pre>

#

### new branch from current branch
git checkout -b <new_branch_name>
