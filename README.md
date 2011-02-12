# cook -- chef-solo with less sit ups

cook wraps the `chef-solo` with saner defaults so you don't have to deal with creating a bunch of configuration files first.

## INSTALL

    curl https://github.com/josh/cook/raw/master/bin/cook > ~/bin/cook
    curl https://github.com/josh/cook/raw/master/example.json > ~/.cook

You don't need to gem install chef, cook bundles it the first time its ran.

## CONFIGURATION

K, so theres some configuration, but just one file.

    $ cat ~/.cook
    {
      "cookbooks": ["http://github.com/josh/osx-cookbooks/tarball/master"],

      "run_list": [
        "git",
        "homebrew"
      ]
    }

`~/.cook` is a standard chief json attributes files with some extra magic. You list your cookbook urls here instead of repeating it as a command line option. Checkout https://github.com/josh/osx-cookbooks to get you started.

## USAGE

    sudo cook

Thats it.
