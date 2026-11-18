# DAY 1 | DEV LOG | TURNING VOL. 01 | STANDARD EBOOKS STYLE

## The Story

There's an epub of the novelingua Turning translation on zlib, which is great but:

- has numerous typos
- is divided by chapter count and not the logical story arcs
- is barebones with no styling

And I aim to fix that!

## What happened today

Set up SSH for the first time! Followed instructions by [W3Schools](https://www.w3schools.com/git/git_security_ssh.asp). Things went okay, except: 

1 - My username has spaces, so instead of `eval $(ssh-agent -s)`, I had to run:

```bash
ssh-agent -a /tmp/ssh-agent.sock > /dev/null
export SSH_AUTH_SOCK=/tmp/ssh-agent.sock
```

instead.

2 - Apparently, after running:

```bash
ssh-keygen -t ed25519 -C "your@email.com"
```

and asked for a file location, you have to type the address out manually without using arrow keys, lest the arrow keys count as part of the address. So I had to type the entire file location letter-by-letter, *WITHOUT* COPYING AND PASTING (actually that'd probably be fine, but I did everything myself just to be sure). It ended up taking 3 tries. The woes!

## What will happen next

I'll probably update this devlog, though the content of each day might vary from a full write-up to just a tweet-like comment! Gotta keep myself pumped ya know?