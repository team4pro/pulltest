# 501k demo site

This website uses Ruby on Rails.

## Git'n started

First, install `git` somehow. On the Mac, you should also install `gitx`.

Then, install `ruby-1.9.2` somehow. If you have `rvm` (*nix):
    rvm install ruby-1.9.2
    rvm use ruby-1.9.2
    rvm gemset create levi

`rvm` is not required though.

Then:
    git clone git@github.com:roy98102/levi.git
    cd levi
    # Answer 'y' if it asks you to trust the .rvmrc file.
    gem env gemdir

If you are using rvm, that should show something like:
    /Users/bgates/.rvm/gems/ruby-1.9.2-p0@levi

Next:
    gem install bundler
    bundle install

Finally,
    rails server -p 3000

Visit:
  http://localhost:3000

You should see the default Rails welcome screen:
> Welcome aboard
> You're riding Ruby on Rails!
> ...

## Development notes.

(I am working on these notes by modifying these notes.)

We are using the *Integration Manager* workflow [Figure 5-2](http://progit.org/book/ch5-1.html). I will write some notes on that after I test it.

1. Develop a feature in a branch.
1. When done, push the branch to your repo.
1. Within your levi fork on GitHub, issue a *pull request*.
1. Anyone can comment on the code. Converse! Look for errors, not style.
1. Any "Integration Manager" (anyone listed as a collaborator on the roy98102/levi repo) will test the commits, as described at GitHub at the bottom of the page where the *pull request* is discussed. It says this:

    > How to merge this pull request (called `feature` from `cdunn2001`):

    1. Check out a new branch to test the changes — run this from your project directory
 
        git checkout -b cdunn2001-feature master

    2. Bring in cdunn2001's changes and test
     
        git pull https://cdunn2001@github.com/cdunn2001/pulltest.git feature
    
    3. Merge the changes and update the server
     
        git checkout master
        git merge cdunn2001-feature
        git push origin master

1. With that, the `feature` branch will *not* be in roy98102, which is good. The changes on it have been merged into the `master` branch.
1. Anyone can then examine their own [*fork queue*](https://github.com/blog/270-the-fork-queue).
1. The submitter may then pull in the latest master from roy98102.

    git fetch origin master
    git checkout master
    git merge origin/master

1. At that point, the submitter may delete the branch from his own repo.

    git br -d feature

Remember: Branch early and often!

