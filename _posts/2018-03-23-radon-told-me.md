---
layout: single
title: 'Radon told me that...'
date: 2018-03-23 9:43:00 -0700
classes: wide
share: false
related: false
---

### So at the end of the last semester, I sent Radon an email...

- - - - - -
Hi Radon,

I'm an HMC frosh living in Fishbowl 1. I am very impressed by your hyper-schedule and your work in GitHub (more accurately, a small subset of your work. I haven't tried Emacs, so I cannot understand half of your GitHub.) Basically, I want to be good at software engineering like you. Do you have any recommendations on how I should start? Is there any extremely useful websites or mindsets you encountered along the way that you would like to share? 

Currently, I have just finished CS42 and I have some competitive programming background (where I write bad but working codes in C++), so I understand and can write basic data structures and algorithms. However, I haven't written a working application/website once, have never used version control, and have never collaborated to make a successful project. So as it is, I feel kind of loss. Currently, I am trying to learn Bash so that I can use the terminal better, but it does not seem to help me that much. Do you have any recommendations of where I should go from here?

Thanks,
Santi.
- - - - - -

### And this was the reply...

- - - - - -
Hi Santi,

Firstly I'd recommend reading [Teach Yourself Programming in Ten Years][ten-years], and then probably [How to Become A Hacker][hacker]. After that, comes years of practice. Here are some things that I think would be good ideas for goals:
- Care about your workflow.
    - Try different text editors. Really try them.
- Learn Emacs and Vim. Learn why people like them, and make your own customizations. I recommend being comfortable in either.
- Learn about dotfiles. Make your own, and put them in version control ASAP. Then put them on GitHub.
- You didn't say what your operating system is. If it's not Linux, learn about Linux.
- Notice inefficiencies in your daily routines. I realized that using Cmd+TAB on a Mac to switch between applications was a waste of time, so I spent some time setting up system-wide hotkeys for every application I use.
- Make tools to solve your problems.
    - straight.el exists because I needed to contribute upstream to the Emacs packages I used, and the built-in package manager didn't let me do that.
    - el-patch exists because I was having trouble keeping track of all the internal functions my Emacs configuration was overriding.
    - Hyperschedule exists because I was considering too many classes during registration for the old hmc-scheduler to handle.
    - smarter-playlist exists because iTunes' Smart Playlist feature wasn't smart enough for me.
    - diary-manager exists because I was learning that keeping a diary in Pages doesn't scale well to hundreds of entries.
    - Radian is the infrastructure that ties together all of these improvements in workflow.
- Learn new things.
    - Learn as many programming languages as you can.
        - Systems programming languages (C, C++, Rust, etc.)
        - Lisps (Common Lisp, Emacs Lisp, Scheme, Clojure, etc.)
        - Functional programming languages (Common Lisp, Clojure, Haskell, etc.)
        - Object-oriented programming languages (C++, Java, C#, etc.)
        - Scripting languages (Python, Ruby, Bash, Zsh)
        - Other kinds of languages (Mathematica, Prolog, Erlang, etc.)
        - The key idea here is that different programming languages can teach you different things. If you can't say you don't think about problems differently after learning a new language, either you haven't learned it or you could have picked a different one to greater effect.
        - Really learn programming languages. Not just superficially. If you're writing C++, read about move semantics, the rule of three/five, template metaprogramming, smart pointers, pointers-to-member, implicit and explicit typecasting, the nuances of how expressions and declarations are parsed (and ambiguities), RAII semantics, public versus private versus protected versus virtual and multiple inheritance, STL algorithms, and so on. (These are just some of the things I investigated since we were using C++ in CS 70; it hardly scratches the surface, though, given the complexity of C++.)
    - Get really good at debugging. Programming is mostly debugging, by time.
        - Sometimes it makes more sense to trace code by hand.
        - Sometimes it makes more sense to just insert print statements.
        - Sometimes it makes more sense to use an actual debugger.
        - Sometimes it makes more sense to just search online or read the documentation.
        - Sometimes it makes more sense to do simple text searches on the code.
        - How do you make accurate guesses about which approach will be the most effective, when by definition you don't know what the problem is?
    - Appreciate systems that have been worked out by previous generations of programmers.
        - Read about version control. Learn why you should use it for everything. Then use it for everything.
            - Read The Git Book.
            - Get really good at Git. Merge, rebase, cherry-pick, plain-text patches, filter-branch, advanced configuration, and so on.
        - Take some time to learn about UNIX. The way the filesystem is integrated into the operating system, and vice versa; symbolic and hard links; FHS; the operation of system package managers; multi-user systems and permissions; users and groups; multi-machine networks; remote login and SSH; shells, executables, arguments; and so on. It's all designed the way it is for a reason.
- Learn soft skills.
    - Learn to write good code that you will still be able to maintain years later.
        - Of my projects, I think the one that comes the closest to this is straight.el.
        - You learn to do this by reading your old code.
    - Learn to write well-architected code that can scale both to increasing demands and changing requirements.
        - I am currently moving to split Hyperschedule into three independent microservices—the frontend, API, and scraper.
        - I learned this primarily by doing a bad job of it during my summer internship at Quantcast.
        - You learn to do this by writing a big project where the requirements are not known at the beginning.
    - Learn to write code that solves real-world problems quickly.
        - I wrote the initial version of Hyperschedule in 30 hours. The only reason this was possible was that at the very beginning, I took the plan and crossed off more than half of the features, leaving only the things that were absolutely necessary.
        - You learn to do this by making a project to solve an ambiguous problem.
    - Learn to balance all three of these considerations, since they are usually at odds.
    - If you can't think of projects, I think solving problems of your own workflow (like I listed above) is a good place to start. You get an immediate benefit, and there is lots of room for improvement.
- Get involved in the open source community.
    - If you don't have a GitHub account, make one. Then put your projects on it. If you don't have any yet, think about making projects that would be helpful (or just interesting) to other people.
    - Find subcommunities that interest you. I contribute to many different Emacs packages, and even a little bit to Emacs itself. I have had discussions on the mailing lists for Emacs, Zsh, and Python's distutils library.
    - Learn to appreciate cultural differences. Projects on GitHub have all sorts of different sizes, goals, characters, maturities, policies, and so on. And there there are the mailing lists (all development on Emacs, Zsh, and even the Linux kernel is done via mailing list)…
These are just some miscellaneous ramblings. They are not particularly well organized. The really important thing is that you devote effort to recognizing what seems to be helpful for you. I have been working consciously on this sort of thinking for many years but I still regularly reassess how I learn, study, and live best. For the very beginning, if you have no idea what to do, I really recommend starting with improving your workflow. Getting started with, say, Emacs or Vim, or a terminal multiplexer, or a better shell (recommended: Zsh), etc. Radian is nothing but configurations for these programs. The software engineering skills you are asking about really only come about once you have done many, many significant projects, and you start to notice trends.

Let me know if you have any further questions, and feel free to forward this email to anyone you feel would benefit from it.

Best regards,
Rаdon.
- - - - - -

### And that was how it went.
And I think I should says thanks sometimes.

[ten-years]: http://norvig.com/21-days.html
[hacker]: http://www.catb.org/esr/faqs/hacker-howto.html