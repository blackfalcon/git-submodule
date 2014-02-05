# Quick and easy git-submodules

> A submodule in a git repository is like a sub-directory which is really a separate git repository in its own right.  This is a useful feature when you have a project in git which depends on a particular versions of other projects. 

[ref](http://longair.net/blog/2010/06/02/git-submodules-explained/)

## WAT?! Why?

Submodules are a really great way to include another Github project into your new project. Why would you want to do this? The best example I can give is, when building a wrapper around another library. 

A recent example where I discovered this was with the implementation of [Node-Sass](https://github.com/andrew/node-sass). Within the project is an interesting reference to the libsass library. 

In other wrappers for the libsass library, the developer forked the whole libssas library and then created the wrapper. This is dangerous, because this requires a lot more work to update the wrapper as the parent library evolves.

## How to create a git-submodule

In this example repo, I created a project that is including the libsass library as a git submodule. The steps are pretty simple:

`$ midir [your-new-project]`

`$ cd [your-new-project]`

`$ git init`

`$ git submodule add https://github.com/hcatlin/libsass`

**BOOM!**

### Your new project

In this example you will see a new directory, `libsass/`. The entire project has been cloned into your local repo for the same of development and it has it's whole git history with it. 

