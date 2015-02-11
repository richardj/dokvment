# Git


## HTTPS and SSH
Oops, used https and now you have to fill out your username and password every time you push?

```
git remote set-url origin *copy the git one*
```

bam! done!

## add / commit / push

Working on something where it doesn't really matter yet whether your codebase is clean? Want to work fast? Just alias it!
Find your .bash_profile / .bashrc or where you store those nice ones and add:

```
alias gogitgetgo="git add -A ; git commit -m 'this is a dangerous commit' ; git push origin master"
```

Because sometimes you don't have time to check your work.
Disclaimer: this can destroy everything you worked for.

## Failing push

Remote repositories can be a weird bunch, when you get the following message:

```
Permission denied (publickey,gssapi-keyex,gssapi-with-mic,keyboard-interactive).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

That might be because you are using a custom key, might have to re-add it, just use:

```
ssh-add path-to-private-key
```

and push away!

