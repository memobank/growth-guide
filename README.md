# Memo Bank's growth guide

Memo Bank's growth guide is a financing guide aimed at established companies that are still growing fast (“scaling“ companies). The guide is maintained by [Memo Bank](https://memo.bank/en), a French bank built by entrepreneurs, for entrepreneurs.

This repository contains the code used to publish our guide at: [guide.memo.bank](https://guide.memo.bank). We use [Jekyll](https://jekyllrb.com) with the [Just the Docs](https://just-the-docs.github.io/just-the-docs/) theme. This site is built using GitHub Actions and served by [GitHub Page](https://pages.github.com).

## A beginner's guide to GitHub

To install and run the guide locally (on your computer) for the first time, follow the steps showcased below. This is going to look a bit nerdy at times, but hang on tight—you'll only have to do most of the following steps _once_.

### Creating a GitHub account

If you haven't created a GitHub account yet, browse to [github.com/signup](https://github.com/signup) and sign up. It's free.

### Downloading the GitHub Desktop app

First you need to know which kind of chip your Mac runs on. To do so, browse to: [support.apple.com/en-us/HT211814](https://support.apple.com/en-us/HT211814)

- If you see your Mac on Apple's list, it means your Mac runs on Apple silicon, so navigate to [desktop.github.com](https://desktop.github.com) and click on the **Download for an Apple silicon Mac**.
- If your Mac isn't listed on Apple's support website, it means your Mac runs on an Intel chip, so navigate to [desktop.github.com](https://desktop.github.com) and click on the main **Download for macOS** button.

Once you've downloaded GitHub Desktop:

1. Go to your Mac's `Downloads` (`Téléchargements`) folder.
2. Double-click the **GitHub Desktop** zip file.
3. Move the **GitHub Desktop** app to your `Applications` folder.
4. Double-click on the **GitHub Desktop** app icon to launch the app.
5. Sign in using your GitHub credentials. You may quit the app after that.

👉 [See GitHub Desktop's documentation](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop)

### Forking the guide

If you want to run the guide on your computer, you'll first need to create your own copy of the guide (your fork). Here's the definition of a fork, according to GitHub's documentation:

> A fork is a copy of a repository that you manage. Forks let you make changes to a project without affecting the original repository. You can fetch updates from or submit changes to the original repository with pull requests.

— [About forks](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks) (GitHub)

Forking the guide will allow you to edit your own personal copy of the guide, without interfering with Memo Bank's version of the guide. We'll see how to sync your fork with Memo Bank's main version, but first let's create your own fork.

To create a fork of Memo Bank's guide:

1. Navigate to: [github.com/memobank/growth-guide](https://github.com/memobank/growth-guide)
2. Click on the **Fork** button (top right corner).
3. Click on **Create fork**.
4. Navigate to your forked repo, which should live at: `github.com/your_user_name/growth-guide`.

👉 [See GitHub's detailed forking guide](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

### Cloning the guide locally

Now that you've forked Memo Bank's guide on github.com, you own a copy of the guide. But for the time being, your copy only lives on github.com. It's a _remote_ copy, not a _local_ one, it lives on GitHub's servers, not on your own computer. To edit your fork on your Mac (locally), you need to download it from github.com. In GitHub's jargon, downloading a remote repository locally is called “making a clone” or just “cloning” it.

Here's the definition of a clone, according to GitHub:

> When you create a repository on GitHub.com, it exists as a remote repository. You can clone your repository to create a local copy on your computer and sync between the two locations.

— [Cloning a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) (GitHub)

To clone your remote fork locally:

1. Navigate to your fork's page (located at `github.com/your_user_name/growth-guide`).
2. Click on the green **Code** button and select **Open with GitHub Desktop**.
3. Click on **Choose…** and select the local folder where you want your fork to live.
4. Click on **Clone** and when asked hit **To contribute to the parent project**.
5. Click on **Continue** and you're done. Good job! You've just cloned your fork locally. 👏

Think as the relationship between all those repos as a triangle:

1. There's **Memo Bank's main repo**, which only lives on github.com, and which you can't edit directly.
2. There's your **remote fork**, which is a copy of Memo Bank's main repo living on github.com, and which you can edit.
3. There's your **local fork**, which is a copy of Memo Bank's main repo living on your computer, and which you can edit too.

### Syncing your fork

GitHub Desktop has done its magic and now your local fork is linked to:

- Memo Bank's main repo (`upstream` in GitHub's jargon). That will allow you to get the latest version of the main repo, in case someone else updates it for example.
- Your remote fork, the one that lives on github.com (`origin` in GitHub's jargon). That will allow you to “push” the edits you made locally on github.com, in order to open a pull request from there—more on that later.

To update your fork:

1. Open **GitHub Desktop** and navigate to your `growth-guide` repository.
2. Click on the **Fetch origin** button and let GitHub Desktop do its magic for you.

Note: if you've just forked our `growth-guide` repository and cloned it on your Mac, then your local clone should be up to date with Memo Bank's main version. Fetching Memo Bank's main repository is only useful if you haven't updated your local fork in a long while.

## Installing and running the guide

Now that the code of our guide lives on your computer, you need to install a few things on your Mac to run the guide locally.

Here's what you'll need to install:

1. Homebrew (a sort of tech App store).
2. Jekyll (the engine that powers our site).
3. Ruby (the language Jekyll is written in).

The good news is: you only have to do these tedious steps once. So hang on.

### Installing Homebrew

Homebrew is a tool that allows you to install other tools on your Mac, using the Terminal. Think of it as an App Store, but for developers.

To install Homebrew, open your Terminal (in `Applications` > `Utilities`). Double click on `Terminal.app`, paste the following line in your Terminal, and hit **Enter**:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

You'll be asked to confirm (hit **Enter** again) and type your macOS user password.

⚠️ Nothing will show up on your screen when you'll start typing your password in the Terminal, that's normal. This is a security feature. Just type your password and hit **Enter** again when you're done.

👉 [See how to troubleshoot common Homebrew errors](https://github.com/lewagon/setup/blob/master/macos.md#homebrew)

Once you've installed Homebrew, paste the following lines in your terminal (all at once). It will install [Git](https://git-scm.com) and [GitHub command line interface](https://cli.github.com) on your Mac.

```
brew upgrade git || brew install git
brew upgrade gh || brew install gh
```

You may quit your Terminal after that (`command` + `Q`).

☝️ Note that “Terminal apps“ don't show up in your `Applications` folder. They're technical tools, not real apps with a visual interface like Slack, iMovie, or Figma.

### Installing Ruby

Start by installing Ruby utilities. Open the Terminal app (in `Applications` > `Utilities`), paste the following line in your Terminal and hit **Enter**. 2.

```
brew install chruby ruby-install xz
```

Then install Ruby itself by pasting the following line in your Terminal and hitting **Enter**.

```
ruby-install ruby 3.1.3
```

Let your Terminal do the work (do not quit it). Installation may take a few minutes. Once new lines stop appearing on your Terminal, it means that Ruby has been installed. You're almost done. Just paste the following lines (all at once) in your Terminal and hit **Enter** one last time.

```
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc # run 'chruby' to see actual version
```

Then quit and reopen your Terminal (to reset it). This is important. And then just paste the following line and hit **Enter**.

```
ruby -v
```

You should see something like: `3.1.3p185 (2022-11-24 revision 1a6b16756e)` or a newer version. If you don't, quit and reopen your Terminal, and then try again (`ruby -v`).

#### Troubleshooting Ruby installation errors

If you get an error that says: `ld: symbol(s) not found for architecture arm64`, try to install Ruby one more time by pasting the following line in your Terminal and hitting **Enter**.

```
ruby-install 3.1.3 -- --enable-shared
```

Again, this might take a while. When you're done, quit your Terminal, restart it, paste the following line and hit **Enter**.

```
ruby -v
```

You should now see something like: `3.1.3p185 (2022-11-24 revision 1a6b16756e)`.

👉 [See Jekyll's installation documentation](https://jekyllrb.com/docs/installation/macos/)

### Installing Jekyll

Jekyll ([jekyllrb.com](https://jekyllrb.com)) is the static site generator behind our guide. Think of Jekyll as the software that turns our Markdown articles (text files) into a complete website with HTML pages (web files).

To install Jekyll on your Mac: open the Terminal app (in `Applications` > `Utilities`), paste the following line and hit **Enter**.

```
gem install jekyll bundler
```

You may quit your Terminal after that (`command` + `Q`).

### Running the guide

You're now all set up to run our guide locally: you've got the code of the guide, you've got a Ruby environment that allows you to run Jekyll, and you've installed Jekyll itself too.

To run the guide on your Mac: Open the GitHub Desktop app. Make sure your current repository is the `growth-guide` repository (top left corner).

Then navigate to `Repository` > `Open in Terminal` or just hit `control` + `<` on your keyboard. Your Terminal will open and set the `growth-guide` as your current directory.

Once you're in the `growth-guide` directory, paste the following line in your Terminal and hit **Enter**.

```
bundle add webrick
```

Then paste the following line and hit **Enter**.

```
bundle exec jekyll serve
```

Navigate to: [http://localhost:4000](http://localhost:4000)

As long as your Terminal is open and running, you can browse your site. To turn your local site off, hit `control` + `C` or just close your Terminal app (`command` + `Q`).

⚠️ The site you're seeing in your web browser is your own copy of Memo Bank's guide. Unlike most websites, this site only lives on your computer. Nobody else can see it, because your site isn't “served” on the web—it's only “served“ on your own Mac.

🤓 You don't have to write the `bundle exec jekyll serve` command on a Post-It note. Let your Terminal do the heavy lifting for you. By hitting the up key (`↑`) when your Terminal is open, you can browse through the Terminal command you previously entered. Since you've just entered the `bundle exec jekyll serve` command, just hit the up key (`↑`) next time you open the Terminal to go back to your `bundle exec jekyll serve` command.

👉 [See the Learn Enough Command Line to Be Dangerous tutorial](https://www.learnenough.com/command-line-tutorial)

## Editing the guide locally

You can edit the guide **locally**, and push your edits on github.com once you're done. Editing the guide locally will allow you to preview your changes in your web browser before pushing them to github.com—on your remote fork. This is ideal if you want to edit the style, content structure, or layout of the guide. To edit the code of the guide locally, you'll need a code editor like Sublime Text.

### Installing SublimeText

To install Sublime Text 4:

1. Browse to: [sublimetext.com](https://www.sublimetext.com) and click on **Download for Mac**.
2. Navigate to your `Downloads` folder (`Téléchargements`) and unzip the Sublime file.
3. Drag and drop `Sublime Text.app` into your `Applications` folder.
4. Double click on `Sublime Text.app` to start the app.

### Configuring Sublime Text

To change the way your code looks in Sublime Text, you may edit Sublime's default settings.

To do so:

1. Open the Sublime Text app.
2. Click on `Sublime Text` (top left corner) and `Preferences` > `Settings`.
3. Two tabs should open. Copy the following code and paste it in the right tab (overwrite the default setting).

```
{
  "font_face": "menlo",
  "font_size": 16,
  "tab_size": 2,
  "translate_tabs_to_spaces": true,
  "detect_indentation": false,
  "ensure_newline_at_eof_on_save": true,
  "trim_automatic_white_space": true,
  "trim_trailing_white_space_on_save": true,
  "draw_white_space": true,
  "draw_unicode_white_space": "punctuation",
  "use_tab_stops": true,
  "hot_exit": false,
  "remember_open_files": true,
  "highlight_modified_tabs": true,
  "rulers": [80],
  "wordWrap": true,
  "folder_exclude_patterns": [
    "tmp",
    "log",
    ".git",
    "_site",
    ".bundle",
    ".sass-cache",
    ".jekyll-cache",
    "build"
  ],
  "theme": "auto",
  "color_scheme": "Breakers.sublime-color-scheme",
  "dark_theme": "Default.sublime-theme",
  "light_theme": "Default.sublime-theme",
  "ignored_packages":
  [
    "Vintage",
  ],
}
```

When you're done, save your new settings (`command` + `S`).

### Installing Sublime packages

Now that you have a brand new code editor, install a few extensions to make Sublime even more powerful. Sublime Text needs to be open for you to install Sublime packages.

#### Package control

Start by installing Sublime Text's package manager.

To do so: navigate to `Tools > Command Palette` (or use `command` + `shift` + `P`). Then Paste the following line in the in the command palette and hit **Enter**.

```
 Install Package Control
```

Quit Sublime Text (`command` + `Q`) and restart it. You can now use Sublime Text's package manager to install packages.

#### Sass

The Sass package will add relevant syntax highlighting to your scss files.

To install the Sass package: navigate to `Tools > Command Palette` (or use `command` + `shift` + `P`). Then Paste the following line in the in the command palette and hit **Enter**.

```
Package control install
```

Then paste:

```
Sass
```

Ensure you've selected the line titled **Sass**, and hit **Enter**.

👉 [See the homepage of the Sass package](https://packagecontrol.io/packages/Sass)

#### Prettier

Prettier will auto-format your code according to rules shared by your colleagues. Think of it as a way to enforce coherence across our many files and projects.

To install the Prettier package: navigate to `Tools > Command Palette` (or use `command` + `shift` + `P`). Then Paste the following line in the in the command palette and hit **Enter**.

```
Package control install
```

Then paste the following and hit **Enter**:

```
Js​Prettier
```

👉 [See the homepage of the Prettier package](https://packagecontrol.io/packages/JsPrettier)

To set up the Prettier package:

1. Click on `Sublime Text` (top left corner).
2. Navigate to `Preferences > Package settings > JsPrettier > Settings – User`.
3. Paste the following code in the tab that opens.

```
{
"auto_format_on_save": true,
}
```

Then save your settings (`command` + `S`).

#### FileIcons

The FileIcons package will replace Sublime Text's default icons with nicer-looking ones.

To install the FileIcons package: navigate to `Tools > Command Palette` (or use `command` + `shift` + `P`). Then Paste the following line in the in the command palette and hit **Enter**.

```
Package control install
```

Then paste the following and hit **Enter**:

```
FileIcons
```

You may restart Sublime Text after that.

👉 [See the homepage of the FileIcons package](https://packagecontrol.io/packages/FileIcons)

### Setting Sublime as your default editor

To tell GitHub Desktop that you're using Sublime Text as your main code editor:

1. Open the GitHub Desktop app.
2. Click on `GitHub Desktop` (top left corner).
3. Navigate to `Preferences > Integrations > External editor`.
4. Make sure **Sublime Text** is set as your external editor.

You may restart GitHub Desktop after that. This will allow you to open files in Sublime Text _directly_ from GitHub Desktop.

### Opening the site's folder in Sublime

To open the site's folder in Sublime Text:

1. Open the GitHub Desktop app.
2. Right click on `Current repository/Growth guide` (top left corner).
3. Click on `Open in Sublime Text`.

Sublime Text should open and you should be able to see the content of the site's folder in your code editor.

### Understanding the GitHub flow

Here's how the typical GitHub flow works in our case:

1. You edit your local copy of the guide (your local fork) using a text editor.
2. You _push_ your edits onto your remote fork (that lives on github.com).
3. You open a _pull request_ to update Memo Bank's main repository using the code you just pushed to your remote fork (which lives on github.com too).

👉 [Learn more about the GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow)

### Creating a new local branch

Think of branches as different versions of the same document. Here's the definition of a branch according to GitHub:

> Use a branch to isolate development work without affecting other branches in the repository. Each repository has one default branch, and can have multiple other branches. You can merge a branch into another branch using a pull request.

— [About branches](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches) (GitHub)

As a general rule, you should not edit your repository's main branch (called `main` or `master`), even if you're the only person working on your fork. The main branch of your repository is your reference branch, it's sacred—you may merge pull requests into it, but you may not edit it _directly_.

So if you want to edit your fork, you'll first create a new local branch in your fork—to keep your main branch clean. The edits will happen on your new branch, not on your main one.

To create a new local branch:

1. Open the GitHub Desktop app.
2. Navigate to the `growth-guide` repository (should be your default one).
3. Click on the `Current branch` tab (top of your screen).
4. Click on the **New branch** outlined button.
5. Name your new branch. Use only small caps and separate words using hyphens. Give it a descriptive name. For example: `edit-bank-loans-article`.
6. Click on the **Create branch** button.
7. If you're asked, choose `Bring my changes to {branch_name}` and hit **Switch Branch**.

Well done, you're now working on a branch that is not your reference branch. You can now mess things up without affecting the main branch of your repository.

### Commit your local changes to your new branch

You've edited a few files locally on your new branch, you've saved your edits in Sublime text. Now what? Well, now you need to “record” your changes. Think of it as taking a picture of what you've changed, in order for you to be able to compare what you now have with what you had before. In Git, taking a picture of your most recent edits is called “making a commit”.

Here's the definition of a commit according to GitHub:

> Similar to saving a file that's been edited, a commit records changes to one or more files in your branch.

— [About commits](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/about-commits) (GitHub)

You can make several commits in a row on the same branch. The smaller your commit, the better. If you've edited the content of an article and the design of a page, it's better to add your text file to a first commit and create a second commit to add your CSS files.

To commit your changes on your local branch:

1. Open the GitHub Desktop app.
2. Select the changed files you'd like to include in your commit.
3. Review your changes using GitHub before/after feature (right panel).
4. Add a descriptive title to your commit (bottom left corner). Keep it short.
5. Add an optional description to your commit message. Explain what you did.
6. Hit the **Commit to {new_branch_name}** button.

Good job. You've created a new _local_ commit on your new local branch. You may repeat this step as many times as needed.

### Pushing your local changes to GitHub

For the time being, your commit only lives on your Mac. At this point, nobody's aware of the edits you just made—except you. For github.com to be aware of the changes you just made, you need to _push_ your commit onto github.com. This amounts to pushing your changes from your _local_ fork to your _remote_ fork, the one that lives on github.com.

To push your local commit onto github.com:

1. Open the GitHub Desktop app.
2. Make sure you're on the branch where you commited your local changes.
3. Hit the **Push origin** button.

Your local commit will be pushed on your github.com fork—which is called `origin` in GitHub's jargon.

👉 [See GitHub's detailed documentation about commits](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project)

### Opening a pull request on github.com

Now that you've edited your github.com fork, GitHub will notice that there's a difference between your remote fork and the main version of the guide (Memo Bank's version).

As a consequence, GitHub will ask if you want to open a pull request in order to integrate your edits into the main version of the guide—Memo Bank's version. Think of pull request as a collaborative review step before the introduction of any change into the main version of the guide.

Here's the definition of a pull request according to GitHub:

> Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

— [About pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) (GitHub)

To create a pull request from your fork:

1. Browse to: [https://github.com/memobank/growth-guide](https://github.com/memobank/growth-guide).
2. Click on **Compare & pull request** button (top of the screen).
3. Give a brief title to your pull request.
4. In the description field, add a comment describing what your changes will introduce. What are you trying to achieve? Why do you want your edits to go live?
5. Hit the **Create Pull Request** button when you're done.
6. Let your teammates know that there's a new pull request open for review.

👉 [See how to create a pull request from a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)

## Editing the guide online

You can also edit the guide **online**, on [github.com](https://github.com/memobank/growth-guide) directly, and create a pull request right in your browser. This won't allow you to preview your changes locally, but it may come in handy if you just want to make a quick content edit in a Markdown file.

To edit a file on github.com:

1. Browse to: [https://github.com/memobank/growth-guide](https://github.com/memobank/growth-guide)
2. Navigate to the file you want to edit and click on the pencil button (top right).
3. Edit the file in your browser.
4. Scroll to the bottom of your screen, up to the `Commit changes` section.
5. Describe what you've just done in a few words on the first line.
6. Add an optional description of what you just did on the second line.
7. Select `Create a new branch for this commit and start a pull request`.
8. Click on **Propose changes**.

Congratulations, you've just created a pull request. If your pull request gets merged, your edit will be integrated into the site's live content.

## Understanding the structure of the site

Contrary to a Google Docs, where you're editing a file that only lives in “the cloud”, GitHub projects can be edited online **or** locally—because they live both online (on github.com) and on your computer (if you cloned a GitHub project locally). As a consequence, you can browse through our site's files either on github.com or locally (using a code editor).

### Content files

Our articles live in Markdown files (`.md`).

- The main `index.md` file, the one that lives at the root of the `growth-guide` folder, contains the text of our main homepage.
- The indicateurs folder contains both our Indicateurs's homepage (`indicateurs/index.md`) and our Indicateurs' articles.
- Same goes for the Garanties and Financements categories, the articles of which live in the `garanties` and `financements` folders, along with their category homepage.
- The `README.md` file contains the copy of the page you're currently reading. That page is only visible on github.com. It does not appear on our guide.
- The `LICENSE.txt` file contains the license of our site. There's no need for you to edit it, but do not delete it.

### Style files

Our site uses the [Just the Docs](https://just-the-docs.github.io/just-the-docs/) theme, a documentation theme designed for Jekyll. What Jekyll does is that it fetches the remote files of the theme when the site is created (built), that's why you **will not** find the theme main stylesheets in our site's folder. In other words, our site's folder only contains the content of our guide. The style applied to our guide lives in the theme's [main repository](https://github.com/just-the-docs/just-the-docs).

That being said, if you want to edit the way our guide looks, you may do so by editing _our_ site directly. That's what the `_sass` folder is made for.

The `_sass` folder contains:

- A `color_schemes/memo.scss` file. Use that file if you want to edit one of the theme's [default variable](https://github.com/just-the-docs/just-the-docs/blob/main/_sass/support/_variables.scss). Do not write custom code in that file.
- A `custom/custom.scss` file. That file hosts all our custom SCSS, that is all the rules that overwrite the theme's default rules. If you want to change a CSS rule, and if there's no default variable for what you want to edit, then add a rule in the `custom.scss` file.

👉 [See the theme's documentation about customization](https://just-the-docs.github.io/just-the-docs/docs/customization/)

### Assets files

The only assets we use are images. They're all located in the `assets/images` folder.

- The `cards` folder contains the images used by Facebook, Twitter, and LinkedIn, to create link previews of our articles.
- The `favicon` folder contains the images used by web browsers to populate tabs and bookmarks with our logo.
- The `logo-memo-bank-white.svg` is Memo Bank's main logo.

### Configuration file

Our Jekyll configuration lives in the `_config.yml` file. There's no need for you to edit that file.

👉 [See the theme's built-in configuration options](https://just-the-docs.github.io/just-the-docs/docs/configuration/)

## TL;DR

Here's how to get started in no time:

1. [Install Ruby and Jekyll on macOS](https://jekyllrb.com/docs/installation/macos/)
2. [Run Jekyll locally](https://jekyllrb.com/docs/)

There's no step 3. 🙂
