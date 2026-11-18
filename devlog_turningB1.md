# DAY 1 | DEV LOG | TURNING VOL. 01 | STANDARD EBOOKS STYLE

## The Backstory

There's an epub of the novelingua Turning translation on zlib, which is great but:

- has numerous typos
- is divided by chapter count and not the logical story arcs
- is barebones with no styling

And I aim to fix that!

The following is a record of what happened today.

## Setting up SSH for Git
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

## Following the [guide](https://standardebooks.org/contribute/producing-an-ebook-step-by-step)

I started the ebook standardizing process by following the above guide, which also seems to be the only guide available on the process (I haven't looked extensively). It starts with an HTML file though - I'm working with an EPUB grabbed with WebToEpub - so I then had to create another folder, working on [Moby Dick](https://github.com/GITenberg/Moby-Dick--Or-The-Whale_2701/blob/master/2701-h/2701-h.htm)[^1] to see what the output of each step is supposed to be like.

> [!TODO]
> Process Turning chapter files extracted from the epub so it looks like the example.

## What will happen next

I'll probably update this devlog, though the content of each day might vary from a full write-up to just a tweet-like comment! Gotta keep myself pumped ya know?

[^1]: Gutenberg was down at the time of writing.