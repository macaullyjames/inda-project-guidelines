# inda-project-guidelines

## Development guidelines
When you're writing code on your own you can pretty much do whatever you like. Bad commit? Eh, `git push -f`. In a rush? You know what you've changed, `lolololol` is a perfectly adequate commit message. Nobody knows and nobody cares.

This kind of anarchy doesn't scale well to teams with more than one member though. You'll be much more productive if you lay down some ground rules based around *respect* and *trust*, like _"Let's make sure we peer review each other's code before pushing to_ `master`_"_ or _"Let's stick to Google's coding conventions so our programming style is consistent"_. You should write these rules down, preferably in a file called CONTRIBUTING.md in the repo.

It's up to you and your team how comprehensive these guidelines are. For example, the CoffeeScript development [guidelines](https://github.com/jashkenas/coffeescript/blob/master/CONTRIBUTING.md) are a four point list. The Auctionet dev team have an entire [handbook](https://github.com/barsoom/devbook) detailing everything from [deploying without downtime](https://github.com/barsoom/devbook/tree/master/deploy_without_downtime) to [how many pizzas to order for a meetup](https://github.com/barsoom/devbook/blob/ddc8c44c045d4c150435b8333b8a213a446e0402/arranging_a_meetup/README.md#order).
For small projects it's enough to make clear:

- How should I contribute code? Send a PR or push to a branch? Do I base off of `master` or some other branch? Should I rebase or merge?
- Is there a style guide I should follow? (No is an OK answer!)

## Setup help
As you probably know by now, having access to a piece of code and being able to build/test/run that code are two different things. You want to make it as simple as possible to get a working dev environment up and running which means clear, unambiguous documentation:

- What OS are you running on? Not just _"Windows/Mac/Linux"_ but an actual description of what I should download, like _"Fedora 23 x64"_.
- What packages/programs are needed? Again, don't say _"Python"_, say _"the_ `dnf` _package_ `python 2.7.10-8.fc23`_"_.
- What libraries do you use? How do I install them? Again, version numbers are important. If at all possible, use a package manager for this (`npm`, `pip`, `CocoaPods` etc.) and store the config files in the repo.
- Finally, how can I build/test/run your code? If you use Eclipse, commit the project files to the repo. If you've written a Bash script, commit that. If you normally just `javac` your way to glory, state that explicitly too.

If possible you should run through your instructions on a clean machine to make sure you haven't missed anything. This doesn't just make life easier for outside contributors, it makes life easier for you too! If you can't reproduce your dev environment, what will you do if your laptop catches fire and/or you spill coffee on it and/or it gets stolen? I'll tell you what: Spend a week crying at the keyboard trying to figure out why Java says `Error: Could not find or load main class Main`. Not fun 🙈

Apart from good documentation, there's a couple of general tips to keep in mind when developing that can save you a lot of headaches later on:

- Simple is good: Do you _really_ have to run a hardened Gentoo installation with a manually patched compiler? Could you not just use Ubuntu 16.04 and `apt-get` a few packages?
- Stick to the language's development conventions. For example, use `npm` instead of Bash scripts if you're writing server-side JavaScript. You're much more likely to find help online if you follow the beaten path.

## Licensing
_Disclaimer: I am not a lawyer_

**Pretty much any original creative work you author is automatically protected under copyright law.** By default, this means that you have exclusive rights to the use and distribution of the work; you get to decide who uses your work, how they use it and their means of obtaining it. **No-one can use your work unless you explicitly allow them too.** It's illegal.

Your source code is an original creative work and as such is protected under copyright law. **Hosting it on GitHub does not change this**, in the same way that posting an article on a blog does not grant readers the permission to re-post the article as their own. This means that **you need to explicitly grant others the rights to use and distribute your code** if you want it to be used in other projects (which you do). **You need a software license**.

Of course, you could write your own software license, but licensing is hard and I'm guessing that you're not a lawyer either. Instead you should choose one of the industry standard licenses such as the MIT, Apache or GPL licenses, depending on how you want your code to be used. If you don't know which license to pick, [choosealicense.com](http://choosealicense.com) is a good place to start. Jeff Atwood's article [Pick a License, Any License](http://blog.codinghorror.com/pick-a-license-any-license/) over on the Coding Horror blog is a good read if you're still not sure.

In summary: It's illegal for others to use your code without a license. Pick a license.
