# Bandit Level 2 -> Level 3

[https://overthewire.org/wargames/bandit/bandit3.html](https://overthewire.org/wargames/bandit/bandit3.html)

> The goal of this level is to find the password stored in a file called spaces in this filename located in the home directory.
>
> After I find the password, I will use that password to log into bandit3 using ssh.

I log in with:

```bash
ssh -p 2220 bandit2@bandit.labs.overthewire.org
```

Once I logged in, I run the command:

```bash
ls
```

After that I find out there is a file named "spaces in this filename" and I tried to run:

```bash
cat spaces in this filename
```

However, this did not work because of the spaces in the file's name.

I found out there are more than one approaches to solve this problem:

```bash
cat "spaces in this filename"
```

```bash
cat 'spaces in this filename'
```

```bash
cat spaces\ in\ this\ filename
```

With that info, I was able to determine the password and proceed to the next level.
