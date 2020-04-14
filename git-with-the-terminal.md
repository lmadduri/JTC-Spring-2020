### Navigation in the terminal

Before we start looking at Git, let's make sure we have enough knowledge
about our terminal to be able to move around folders and files.

#### `pwd`

If you're a Mac user, in your terminal, type `pwd` and
press enter. This is the first of several **commands** we'll cover, and
it shows you exactly where you are in your terminal. That's why the
command is called `pwd`: it stands for Print Working
Directory.

Windows users won't have to worry about `pwd`, because
Command Prompt will always show your complete location.

<span class="major-key">If you're ever confused or want to learn more
about a specific command, just run `man [command]` on
Macs, or `HELP [command]` on Windows</span>. For example,
you can type `man ls` and you'll see more information than
you'd ever want to know about `ls`! On Macs, you'll have
to press `q` in order to exit the manual view.

#### `ls`

Once you've figured out what directory you're in inside your terminal,
run `ls` (`dir` on Windows). You'll see a
list of all the files and folders inside your current directory.

#### `cd`

Now that you can see all your files and folders, we'll talk about
navigating between folders. If you've just run `ls` or
`dir`, you'll be able to see a bunch of folders, like
Documents and Downloads. Try running `cd Documents` now.
This will bring you into the Documents folder, and you can
`ls` or `dir` to see how poorly organized
your Documents folder is.

To get back to where you were, type `cd ..`:
`..` always stands for the parent directory, and
`.` always stands for the current directory.

OK, now we're ready to get started with git!

<a id="intro-git"></a>
### Creating and cloning your first repo

First, login to GitHub and create a new **repository**. Name the
repository \[your-username\].github.io, make it public, and check the box
that says “Initialize this repository with a README”.

Once you've created the repository (**repo** for short), GitHub will
take you to the repo's freshly created page. Find the box on the page
that contains a link, which should look something like `https://github.com/adicu/density.git`.

Copy the link, then open your terminal, navigate to a folder where
you're comfortable keeping coding projects, and run the following
command:

    git clone [link-you-copied]

This will copy the repository and all its contents onto your computer,
and it'll create a new folder inside whatever folder you ran
`git clone` from.

You can do this with any project on GitHub, whether or not it belongs to
you. People who use GitHub to store their projects are participating in
**open source** development, so that everyone can contribute to everyone
else's projects. Now you're entering into that world!

<a id="committing"></a>
### Committing changes to a project

While you should still be saving your work habitually, Git enables you
to create certain checkpoints. Whenever you feel that you've completed a
task, solved a problem, or you just want to save the work that you've
done as a complete unit, you make a Git **commit**.

There are a couple of different steps to doing this. First, let's get
our repository to a state that's ready to be committed. Right now, if
you `ls` or `dir` inside the directory you
just cloned, there should only be one file: README.md. Let's fix that by
adding an `index.html`! You can either reuse your HTML
from our assignments or create something new, but it doesn't matter as
long as you save it in your `username.github.io` folder.

#### `git status`

Now, try running the following command: `git status`. Your
terminal will respond with some information; importantly, it tells us
that we have “untracked files”. Don't worry about the other information
for now.

`git status` is a really important command, because it
shows us what Git thinks the current state of the repository is. It's a
powerful debugging tool, and also helps us understand what other git
commands are actually doing behind the scenes.

#### `git add`

Let's run another command: `git add index.html`. Now, if
we run `git status` again, we'll see that we no longer
have any untracked files; instead, we have a section called “Changes to
be committed”, and it tells us that Git is now aware of a new file
called `index.html`. `index.html` is now
**staged** to be committed.

You can stage all of the files in a directory by running
`git add -A`.

#### `git commit`

So what does it mean for a file to be staged to be committed? It means
that if we run `git commit`, our changes will be included
in that commit, which, like I mentioned before, is essentially a
checkpoint for our repo. Let's do this now by running
`git commit -m "Create index.html"`. Whenever you make a
commit, you include a commit message that explains the changes you've
made, and it goes inside quotes after `-m`.

#### `git log`

If you run `git log`, you'll see the entire history of
your repository. Now that you've committed something, the log will
contain two commits: the initial commit, made on GitHub, and your own
commit, “Create index.html”.

#### `git push`

So far, all of these commands have only been relevant to our local work.
But the magic of Git is that it makes it really easy to share your code
with other people and store it in one centralized location. Run
`git push origin master` and watch the magic unfold! It'll
print some garbage, like
`Delta compression using up to 4 threads`, but what's
important is that it gets your **remote** repository (i.e., GitHub's
version) up to the same point as your local repo. The GitHub page for
your repo will reflect the changes you've made.

<a id="workflow"></a>
### Developing a Git workflow

These commands are all you need to maintain a repo on your own. <span
class="major-key">You should develop a consistent workflow with
Git, and it should look something like this</span>:

1.  Do some good work.
2.  `git add`: Most of the time, you'll use
    `git add -A`, but you can specify individual files if
    need be.
3.  `git commit -m "Extra informative commit message"`
4.  `git push origin master`
5.  Repeat steps 1–4 until code is perfect

#### `git diff`

There's another command that will be helpful to you as you start to work
with bigger and bigger files and projects. Running
`git diff` will show the differences between the lines of
code in your currently saved files and the code from your most recent
commit. If you ever spend more than an hour working on something, you'll
probably find yourself wondering what's actually changed and how it's
changed before you want to `git add` anything. This is a
great way to ensure that you're only committing exactly the code you
want to commit.

--------------

This lesson was a little shorter, but there's still a lot of technical
language to learn!

<a id="terms-git"></a>
### Git terms you should know

Git
:   A version control system developed by Linus Torvalds in 2005.

version control
:   Software that makes it easy to organize and control revisions.

command
:   A program you can run from the command line. You should be familiar
    with `pwd`, `ls` (or
    `dir`), `cd`, and `subl`.

Repository (repo)
:   A folder that contains a project that's tracked by Git.

GitHub
:   A platform that hosts Git projects and facilitates open
    source collaboration.

staged
:   Describes changes that are ready to be committed.
    `git add` stages your changes.

commit
:   A savepoint in Git history.

remote
:   A version of a Git project that is hosted on an outside network.
    GitHub contains the remote version of your username.github.io repo.

Git commands to be familiar with:

:   -   `git status`: current state of the git repo
    -   `git add`: stage files for being committed
    -   `git commit`: save all staged files into a
        definitive savepoint
    -   `git log`: shows commit history
    -   `git push`: pushes local commits to remote
    -   `git diff`: shows difference between repo and most
        recent commit

<a id="project-git"></a>
### Do things with Git

Like I said before, it's really important to develop a consistent workflow with Git. So, now that your `index.html` has been committed, a great way to practice will be to commit the rest of the files you've worked on this week!


#### Committing the rest of your work

You should definitely review the workflow I outlined earlier. You'll need to copy the files and directory structure into your `[username].github.io` folder, then `add`, `commit`, and `push` everything.

Once you've done this, navigate to `[username].github.io` in your browser: surprise!
Now your website is live and viewable to anyone with an Internet connection.
GitHub hosts a free website for all of its users, because they are an
amazing company.
