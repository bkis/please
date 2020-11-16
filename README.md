# please :pray:

A polite companion that helps noting exotic terminal one-liners :woman_technologist:

![demonstrational animation](https://user-images.githubusercontent.com/9215743/77434881-d06b8d00-6de1-11ea-8ec1-6440c9d6436b.gif)

- [please :pray:](#please-pray)
  - [What is this?](#what-is-this)
  - [What does it do? How do I use it?](#what-does-it-do-how-do-i-use-it)
  - [Why would I ever use this instead of just creating aliases for my one-liners?](#why-would-i-ever-use-this-instead-of-just-creating-aliases-for-my-one-liners)
  - [Installation](#installation)
  - [Command overview](#command-overview)
  - [Contribution](#contribution)

## What is this?

**please** is a **bash script**. Just one file, very simple. It takes only a handful of arguments. But, more importantly ...

## What does it do? How do I use it?

**please** is an easy way to note and find terminal one-liners right in the terminal. Imagine you spent a good ten minutes to search the web for the perfect terminal one-liner to _raise the audio volume of a video file_ and found `ffmpeg -i "$videofile" -vcodec copy -af "volume=12dB" "louder_$videofile"`. Sweet!  
Of cource, next time you need this you are gonna spend the same ten minutes to look for this precious intel again _(unless you remembered it, which we both know you didn't)_.  
**OR** you could just type `please note how to ...`:

![please note how to](https://user-images.githubusercontent.com/9215743/77423182-094e3680-6dcf-11ea-8352-d13a09827472.png)

So you ask **please** to note something, it asks you back for your one-liner, done.  
And yes, that's the command syntax. A natural language sentence. I could have made it `please -s "raise the audio volume of a video"`, but I didn't want to - and the one who has to deal with that is you. Anyway, what now? Well, just search for a keyword using `please look for ...`:

![please look for](https://user-images.githubusercontent.com/9215743/77423189-09e6cd00-6dcf-11ea-86ac-ab503cf3abdd.png)

... and it will list all your noted one-liners that contain the given keyword.

## Why would I ever use this instead of just creating aliases for my one-liners?

Well, first of all, no one forces you to use it, so sit back down and try to breathe steadily. Here are a few possible answers:

-   Not everyone is a natural pro-hacker-6000™ and some don't even want to become one. For some people, adding aliases in `.bashrc` (or similar) wouldn't be the most obvious workflow. Instead, whenever the occasional terminal user might **struggle to remember this almighty one-liner** they found online five years ago to resize 20469 holiday photos in one go, they can **just type** `please look for "crop image"` (the quotes are actually optional) to get a list of their relevant noted one-liners.
-   It's **fun** to use a command line tool with such a _**natural, friendly syntax**_ for a change. It really is!
-   This is _**not**_ for managing your everyday commands! Obviously, this tool is not really useful for remembering `ls -lah` or the like. You'll want to create an alias for this, I understand. But what about `ffmpeg -i "$video-file" -vcodec copy -af "volume=12dB" "loud_$video-file"` (the example from [above](#what-does-it-do-how-do-i-use-it)), which raises the audio volume of a video file by 12dB while not touching the video signal? Will you use that daily? Will you remember it after some weeks? :thinking: No, you'll start searching the internet for it.
-   Go ahead, collect your hundreds of aliases in your `.bashrc` over the years. An then when you need one of them, of course you won't remember it, forcing you to search your aliases.
-   It has colors :rainbow::open_mouth: The colors and the font styling make it very cool and readable (and cool).

## Installation

1.  _Relax, it's very simple._ :man_shrugging:
2.  Put the `please` file wherever you want it to be. This might be your home directory (`~`) or any other place.
3.  Open a terminal and `cd` to wherever you put `please` (if you're not already there)
4.  Run `./please install yourself`. This will do two things:
    1.  It will create a `~/.please` file (that's where your one-liners and their descriptions are stored).
    2.  It will append an alias entry to your `~/.bashrc` file, so that you can run `please` from anywhere without using the full path and the `./`.
5.  Close the terminal session and start a new one!
6.  Run `please help` to get a list of commands!
7.  Get into the habit of (_kindly_) asking **please** to note one-liners for you!

> :warning: **BTW** if you want the `please`-alias to be added to a file other than `.bashrc`, you can change the variable `PLS_BASHRC` in the script to something else (preset is `${HOME}/.bashrc`).

## Command overview

![command overview](https://user-images.githubusercontent.com/9215743/77440789-fd6f6e00-6de8-11ea-909e-250d0387cae8.png)

## Contribution

This is just a very small weekend projekt I started when I had to stay inside for isolation from the Corona virus and I was in the mood to work on something simple that I could actually finish and document really quickly. It was fun.  
**But I am far from experienced in writing shell scripts.** If you want to improve this in any way, you're welcome to do so! It's very easy to get a grasp of what is happening in the code, so I think it's a nice playground to practice stuff like this and make something potentially useful.

Just **_fork_**, **_clone_**, **_branch_**, **_hack_**, **_commit_**, **_push_** and **_create a pull request_** :woman_technologist:
