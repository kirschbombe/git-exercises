---
title: Ignoring Things
teaching: 5
exercises: 0
questions:
- "How can I tell Git to ignore files I don't want to track?"
---

> ## Ignoring Nested Files
>
> Given a directory structure that looks like:
>
> ~~~
> results/data
> results/plots
> ~~~
> {: .bash}
>
> How would you ignore only `results/plots` and not `results/data`?
>
> > ## Solution
> >
> > As with most programming issues, there are a few ways that you
> > could solve this. If you only want to ignore the contents of
> > `results/plots`, you can change your `.gitignore` to ignore
> > only the `/plots/` subfolder by adding the following line to
> > your .gitignore:
> >
> > `results/plots/`
> >
> > If, instead, you want to ignore everything in `/results/`, but wanted to track
> > `results/data`, then you can add `results/` to your .gitignore
> > and create an exception for the `results/data/` folder.
> > The next challenge will cover this type of solution.
> >
> > Sometimes the `**` pattern comes in handy, too, which matches
> > multiple directory levels. E.g. `**/results/plots/*` would make git ignore
> > the `results/plots` directory in any root directory.
> {: .solution}
{: .challenge}

> ## Including Specific Files
>
> How would you ignore all `.data` files in your root directory except for
> `final.data`?
> Hint: Find out what `!` (the exclamation point operator) does
>
> > ## Solution
> >
> > You would add the following two lines to your .gitignore:
> >
> > ~~~
> > *.data           # ignore all data files
> > !final.data      # except final.data
> > ~~~
> > {: .output}
> >
> > The exclamation point operator will include a previously excluded entry.
> {: .solution}
{: .challenge}

> ## The Order of Rules
>
> Given a `.gitignore` file with the following contents:
>
> ~~~
> *.data
> !*.data
> ~~~
> {: .bash}
>
> What will be the result?
>
> > ## Solution
> >
> > The `!` modifier will negate an entry from a previously defined ignore pattern.
> > Because the `!*.data` entry negates all of the previous `.data` files in the `.gitignore`,
> > none of them will be ignored, and all `.data` files will be tracked.
> >
> {: .solution}
{: .challenge}

> ## Log Files
>
> You wrote a script that creates many intermediate log-files of the form `log_01`, `log_02`, `log_03`, etc.
> You want to keep them but you do not want to track them through `git`.
>
> 1. Write **one** `.gitignore` entry that excludes files of the form `log_01`, `log_02`, etc.
>
> 2. Test your "ignore pattern" by creating some dummy files of the form `log_01`, etc.
>
> 3. You find that the file `log_01` is very important after all, add it to the tracked files without changing the `.gitignore` again.
>
> 4. Discuss with your neighbor what other types of files could reside in your directory that you do not want to track and thus would exclude via `.gitignore`.
>
> > ## Solution
> >
> > 1. append either `log_*`  or  `log*`  as a new entry in your .gitignore
> > 3. track `log_01` using   `git add -f log_01`
> {: .solution}
{: .challenge}
