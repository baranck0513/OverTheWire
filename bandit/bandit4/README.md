# Bandit Level 3 -> Level 4

[https://overthewire.org/wargames/bandit/bandit4.html](https://overthewire.org/wargames/bandit/bandit4.html)

> The goal of this level is to find the password stored in a hidden file in the inhere directory.
>
> After I find the password, I will use that password to log into bandit4 using ssh.

I log in with:

```bash
ssh -p 2220 bandit3@bandit.labs.overthewire.org
```

Once I logged in, I run the command:

```bash
ls
```

I see there is a directory named "inhere". I navigated into that directory using:

```bash
cd inhere
```

I tried to run the "ls" command. However, nothing came up. Then I tried to run:

```bash
ls -l
```

And I saw a file named "...Hiding-From-You".

I tried to read that file using:

```bash
cat ./...Hiding-From-You
```

With that info, I was able to determine the password and proceed to the next level.
