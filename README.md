# Handling submodules

after checking out this repo:
    
    git submodule init
    
adding more submodules this repo:
    
    git submodule add 'https://github.com/user/repo/'
    
to update the submodules:
    
    git submodule update
    
I am not sure if this is necessary for every submodule

    # cd submod/
    git checkout master
    
    
For removal see https://chrisjean.com/git-submodules-adding-using-removing-and-updating/
    
> Sticking with the example, we’ll remove the lib/billboard module from
> SampleTheme. All the instructions will be run from the working
> directory of the SampleTheme repository. In order, we need to do the
> following:

> 1. Remove the submodule’s entry in the .gitmodules file.Since
> lib/billboard is the only submodule in the SampleTheme repository, we
> can simply remove the file entirely by running “git rm
> lib/billboard”.If lib/billboard isn’t the only submodule, the
> .gitmodules file will have to be modified by hand. Open it up in vi,
> or your favorite text editory, and remove the three lines relevant to
> the submodule being removed. In this case, these lines will be
> removed:

>     [submodule “lib/billboard”] 
>     [path = lib/billboard 
>     [url = git@mygithost:billboard

> 2. Remove the submodule’s entry in the .git/config. This step isn’t
> strictly necessary, but it does keep your config file tidy and will
> help prevent problems in the future.The submodule’s entry in
> .git/config will only be present if you’ve run “git submodule init”
> on the repository. If you haven’t, you can skip this step.In this
> example, the following lines will be removed:
    
>     [submodule “billboard”] url = git@mygithost:billboard

> 3. Remove the path created for the submodule. This one is easy. Simply
> run “git rm –cached [plugin path]“. In this example, I will run “git
> rm –cached lib/billboard“.As I’ve seen noted elsewhere, do not put a
> trailing slash as the command will fail. For example, if I run “git
> rm –cached lib/billboard/“, I get an error: “fatal: pathspec
> ‘lib/billboard/’ did not match any files“.

    




    