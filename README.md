# Emu #

> Helper framework that has automation using [Gulp](http://gulpjs.com/) for the build process (compression, compilation and browser syncing) and [Bourbon and Neat](http://bourbon.io/) (maintained and funded by [thoughtbot, inc](https://thoughtbot.com/)) for the SCSS framework.


### What is this repository for? ###

Speeding up prototyping and building of web applications.
Use the documentation on the http://bourbon.io/ website if you haven't used it before.


# Getting Started #

To get started download [Emu](https://github.com/nilssanderson/emu) with Git:
```
git clone --recursive https://github.com/nilssanderson/emu.git
cd emu
npm install
```

If you have already cloned the repository and the submodule has not been pulled down, then run:
```
cd emu
git submodule update --init --recursive
```

Then to build the framework:
```
gulp
```

The default task should:

* Convert SCSS to CSS
* Compress Images
* Open these in the browser for syncing

Your finished site will be created in a folder called `build`, viewable at this URL: [http://localhost:3010](http://localhost:3010)

* Browsersync settings: [http://localhost:3020](http://localhost:3020)

To create compressed, production-ready assets, run:
```
gulp production
```


# Adding the framework as a submodule #

Delete the app folder and update the gulpfile srcPath to 'YOUR_SRC_PATH' so you can keep your files where they are.

Follow the below instructions to add the framework to an already existing project and to keep it separate from your current repository:
```
git submodule add https://github.com/nilssanderson/emu.git emu
git submodule init
git submodule update
```

Once the framework has been added in as a submodule, a `.gitmodules` file will be created. You will need to specify the branch that you wish to track on the framework. Edit the `.gitmodules` file to include the branch:
```
[submodule "emu"]
	path = emu
	url = https://github.com/nilssanderson/emu.git
	branch = master
```

Run this if there have been any updates to the [Emu](https://github.com/nilssanderson/emu) framework to pull down the latest changes:
```
git submodule update
```

A detached HEAD state may occur when updating a submodule. Once an update has been run, just make sure that the submodule is tracking the `master` branch:
```
cd emu
git checkout master
```

> Some more info that could be looked into in regards to improving submodule addition:
 [Stackoverflow - Answer 1](http://stackoverflow.com/questions/1777854/git-submodules-specify-a-branch-tag/18797720#18797720) and [Stackoverflow - Answer 2](http://stackoverflow.com/questions/1777854/git-submodules-specify-a-branch-tag/18799234#18799234)
