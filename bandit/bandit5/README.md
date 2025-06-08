# Bandit Level 4 -> Level 5

[https://overthewire.org/wargames/bandit/bandit5.html](https://overthewire.org/wargames/bandit/bandit5.html)

> The goal of this level is to find the password stored in the only human-readable file in the inhere directory.
>
> After I find the password, I will use that password to log into bandit5 using ssh.
>
> But there was a tip that website has given me. It was stated that "if your terminal is messed up, try the “reset” command.". This made me think there might be a lot of files to check.

I logged in with:

```bash
ssh -p 2220 bandit4@bandit.labs.overthewire.org
```

Once I logged in, I ran the command:

```bash
ls
```

I saw a directory named inhere, so I navigated into it using:

```bash
cd inhere
```

I ran ls again and saw 10 files named like -file00, -file01, and so on. I opened them one by one using:

```bash
cat ./-file00
```

However, none of them immediately showed the password. I kept checking them individually. 

Eventually, I found the password in one of the files, but I realized this approach wouldn’t be efficient if there were a large number of files to check. 

Since I knew the file with the password was an ASCII text file (human-readable), I looked for a command to identify such files. I tried:

```bash
find ./* | grep ASCII
```

This command helped me locate the file that contained ASCII text and that’s where I found the password. 
