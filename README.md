# Intro

TBA

# Work locally

Install the runtime:

``` sh
brew install rbenv ruby-build
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
source ~/.bash_profile
rbenv install 
rbenv global 
gem install bundler
```

In the directory where you want to keep the project:

``` sh
git clone git@github.com:eic-network/eic-network.github.io
cd eic-network.github.io
bundle install
```

Now start the local instance you just cloned:

``` sh
bundle exec jekyll serve
```

That's it! Now go to:

* http://localhost:4000 for the site
* http://localhost:4000/admin for the administrative UI to manage the content

# Sync changes

This site contents are versioned through Git, so Git specific workflows are applicable. The simplest example would be:

``` sh
# After you have edited some files / templates / contents, check to see what changed
git status

# To look closer at the changes, do a diff against the last committed version. Exit the pager with `q`.
git diff

# Add all the changes to the Git staging area
git add .

# Create a Git commit to save the added changes
git commit -m 'Edited something in an article and added some more'

# Send the local commit(s) to the Git remote (GitHub etc.) so it's propagated to the deploy site
git push
```

# Privacy warning

Everything in this repository is public due to limitations of the free tier for GitHub accounts. Make sure nothing sensitive is ever added to it and use the proper channels for such communications / drafts / private materials.

For drafting purposes, just use your local environment until publishing:

``` sh
# Create a new branch for the private work and switch to it
git checkout -b some-new-article

# now do your work here, modify things etc.
git add .
git commmit -m 'Some secret work'

# Do NOT push it, it's secret! Switch back to master now.
git checkout master

# If you ever want to get back to your secret work:
git checkout some-new-article

# When you are done with it, merge it into master:
git checkout master
git merge some-new-article
git push
```
