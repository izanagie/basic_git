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
GitHub recently changed the default branch on new repositories from master to main. Change the default branch for Git using this command:

```
git config --global init.defaultBranch main
```
To enable colorful output with git, type

```
git config --global color.ui auto
```
You’ll also likely want to set your default branch reconciliation behavior to merging. You’ll learn what all those terms mean later in the curriculum, but for now just know that we suggest running the below command as part of the Git setup process when doing The Odin Project.

```
git config --global pull.rebase false
```
To verify that things are working properly, enter these commands and verify whether the output matches your name and email address.

```
git config --get user.name
git config --get user.email
```
### 1.3 Create an SSH Key
An SSH key is a cryptographically secure identifier. It’s like a really long password used to identify your machine. GitHub uses SSH keys to allow you to upload to your repository without having to type in your username and password every time.

First, we need to see if you have an Ed25519 algorithm SSH key already installed. Type this into the terminal and check the output with the information below:

```
ls ~/.ssh/id_ed25519.pub
```
If a message appears in the console containing the text “No such file or directory”, then you do not yet have an Ed25519 SSH key, and you will need to create one. If no such message has appeared in the console output, you can proceed to step 1.4.
To create a new SSH key, run the following command inside your terminal.

```
ssh-keygen -t ed25519 -C "your@email.com"
```
### 1.4 Link your SSH key with GitHub

Now, you need to tell GitHub what your SSH key is so that you can push your code without typing in a password every time.

First, you’ll navigate to where GitHub receives our SSH key. Log into GitHub and click on your profile picture in the top right corner. Then, click on Settings in the drop-down menu.

Next, on the left-hand side, click SSH and GPG keys. Then, click the green button in the top right corner that says New SSH Key. Name your key something that is descriptive enough for you to remember where it came from. Leave this window open while you do the next steps.

Now you need to copy your public SSH key. To do this, we’re going to use a command called cat to read the file to the console. (Note that the .pub file extension is important in this case.)

```
cat ~/.ssh/id_ed25519.pub
```
Highlight and copy the output, which starts with ssh-ed25519 and ends with your email address.

Now, go back to GitHub in your browser window and paste the key you copied into the key field. Keep the key type as Authentication Key and then, click Add SSH key. You’re done! You’ve successfully added your SSH key!






