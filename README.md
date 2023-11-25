# basic_git
Some basic git instrusctions refered from the odin project.
These are some basic instructions copied as it is from The Odin Project for setting up git locally.
(for arch-linux based systems)
## Step 1: Install Git
### 1.1 Install Git
if git isnt installed already (chances are rare) do
```
sudo pacman -S git
```
### 1.2 Setup a Git
Assuming we already have a github account, we need to let know who we are so that it can link a local Git user (you) to GitHub. When working on a team, this allows people to see what you have committed and who committed each line of code.

The commands below will configure Git. Be sure to enter your own information inside the quotes (but include the quotation marks)!

```
git config --global user.name "Your Name (username)"
git config --global user.email "yourname@example.com"
```
If you opted to use the private GitHub email address, the second command will look something like this:

```
git config --global user.email "123456789+odin@users.noreply.github.com" # Remember to use your own private GitHub email here.
```



