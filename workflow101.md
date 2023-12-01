# workflow 101

### Github ssh-key setup

1. check your account: click on your avatar→settings→SSH and GPG keys(left sidebar)→confirmed SSH keys are empty
2. check if /.ssh folder is empty, if not delete all files inside

```jsx
rm -rf ~/.ssh/*
```

1. (optional)these 2 commands you can skip if you never set config before because these for resetting

```jsx
git config --unset-all user.email
git config --unset-all user.name
```

1. generate ssh-key on your local machine, “your_email” should be your github registration email, and hit **3 times of ENTER** on your keyboard(empty input for 3 questions)

```jsx
ssh-keygen -t rsa -b 4096 -C "your_email"
```

1. set config on your local machine

```jsx
git config --global user.email "your_email"
git config --global user.name "your_username"
```

1. copy and paste the string from the following command to the step1’s place(github’s SSH key)

```jsx
cat ~/.ssh/id_rsa.pub
```

### Contribute to Repo

1. find a folder you want to place the repo and sync your local machine with the remote repo

```jsx
git clone "SSH link"
```


2. Create a issue on the issue section on github, and **relink it on the main markdown file**, put all used screenshots of figures in DDIA to the img folder

3. my commonly used git operations:

  - check if all the things up-to-date

```jsx
git pull
```

  - check the status of all files, if it’s red, meaning not committed

```jsx
git status
```

  - add all changes to staging area

```jsx
git add -A
```

  - commit all changes to local repo, with a comment in “”

```jsx
git commit -m "your comment"
```

  - push all changes to the remote repo

```jsx
git push
```

4. when you want to quote the images you uploaded in the img folder, remember to change the DDIA-notes/**blob**/main/ in the link to DDIA-notes/**raw**/main/ after directly copying from browser.
