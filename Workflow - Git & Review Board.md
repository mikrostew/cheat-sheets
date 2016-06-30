<html>
<head>
<style>
pre {
background-color: #D9D9D9;
}
</style>
</head>
<body>

## Workflow - Git & Review Board

Adapted from [https://iwww.corp.linkedin.com/wiki/cf/pages/viewpage.action?pageId=124791125](https://iwww.corp.linkedin.com/wiki/cf/pages/viewpage.action?pageId=124791125)

<div style="float:left; width: 47.5%">

### Before starting

Create and checkout a new branch:

<pre style="margin-left: 10px; margin-right: 20px;"> git checkout -b &lt;branch-name&gt;
</pre>

### Commit in small chunks

I find it easiest to use the gui for stage/commit/revert:

<pre style="margin-left: 10px; margin-right: 20px;"> git gui
</pre>

### Periodically rebase

This ensures that your work doesn&rsquo;t conflict with what&rsquo;s in the repo. Doing this as you work makes for an easier pre-commit rebase later:

<pre style="margin-left: 10px; margin-right: 20px;"> git checkout master
 git pull --rebase
 git checkout <branch-name>
 git rebase master
</pre>

### Create the RB

Set your branch to track origin/master

<pre style="margin-left: 10px; margin-right: 20px;"> git branch &lt;branch-name&gt; -u origin/master
</pre>

Create the review board:

<pre style="margin-left: 10px; margin-right: 20px;"> git review
</pre>

### Updating the RB

Commit to the branch like normal, then update like so:

<pre style="margin-left: 10px; margin-right: 20px;"> git review update
</pre>

</div>

<div style="float:left; width: 47.5%; margin-left: 4%;">

### Squash commits (after getting ship-its)

Squash your commits into a single commit, to keep a clean history, and make reverting easier:

<pre style="margin-left: 10px; margin-right: 20px;"> git rebase -i HEAD~&lt;number-of-commits&gt;
</pre>

I usually `pick` the first one, and `squash` the rest.

### Apply RB to your commit

<pre style="margin-left: 10px; margin-right: 20px;"> git review dcommit
</pre>

### Rebase your branches

If you&rsquo;ve been doing this periodically, this should be painless:

<pre style="margin-left: 10px; margin-right: 20px;"> git pull --rebase origin master
 git checkout master
 git pull --rebase
</pre>

### Merge into master

This step ensures that the ACL and RB checks go smoothly:

<pre style="margin-left: 10px; margin-right: 20px;"> git merge &lt;branch-name&gt;
</pre>

### Push your changes

Finally!

<pre style="margin-left: 10px; margin-right: 20px;"> git submit
</pre>

### You&rsquo;re done!

Almost - you should still check go/crt. When all of the boxes are green, then you&rsquo;re done for real.

</div>

</body>
</html>
