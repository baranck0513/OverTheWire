# Bandit Level 0 -> Level 1

[https://overthewire.org/wargames/bandit/bandit1.html](https://overthewire.org/wargames/bandit/bandit1.html)

> The goal of this level is to find the password stored in a file called readme located in the home directory.
>
> After I find the password, I will use that password to log into bandit1 using ssh.

I log in with:

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```

Once I logged in, I run the command:

```bash
ls
```

After that I see, there is a file named "readme" and I run the the command:

```bash
cat readme
```

With that info, I was able to determine the password and proceed to the next level.
