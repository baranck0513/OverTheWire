# Bandit Level 1 -> Level 2

[https://overthewire.org/wargames/bandit/bandit2.html](https://overthewire.org/wargames/bandit/bandit2.html)

> The goal of this level is to find the password stored in a file called - located in the home directory.
>
> After I find the password, I will use that password to log into bandit2 using ssh.

I log in with:

```bash
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

Once I logged in, I run the command:

```bash
ls
```

After that I find out there is a file named "-" and I tried to open that file using:

```bash
cat -
```

However, it did not work as I expected. 

After doing a research for a while, I find out that using "cat -" means "read from the standard input (stdin)". 

To solve this problem, I needed to specify the absolute path of that file. So, I used:

```bash
cat ./-
```

With that info, I was able to determine the password and proceed to the next level.


[Reference](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)
