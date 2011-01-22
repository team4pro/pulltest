# demo site

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


