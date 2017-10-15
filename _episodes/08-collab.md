---
title: Collaborating
teaching: 25
exercises: 0
questions:
- "How can I use version control to collaborate with other people?"
---

> ## Switch Roles and Repeat
>
> Switch roles and repeat the whole process.
{: .challenge}

> ## Review Changes
>
> The Owner push commits to the repository without giving any information
> to the Collaborator. How can the Collaborator find out what has changed with
> command line? And on GitHub?
>
> > ## Solution
> > On the command line, the Collaborator can use ```git fetch origin master```
> > to get the remote changes into the local repository, but without merging
> > them. Then by running ```git diff master origin/master``` the Collaborator
> > will see the changes output in the terminal.
> >
> > On GitHub, the Collaborator can go to their own fork of the repository and
> > look right above the light blue latest commit bar for a gray bar saying
> > "This branch is 1 commit behind Our-Respository:master." On the far right of
> > that gray bar is a Compare icon and link. On the Compare page the
> > Collaborator should change the base fork to their own repository, then click
> > the link in the paragraph above to "compare across forks", and finally
> > change the head fork to the main repository. This will show all the commits
> > that are different.
> {: .solution}
{: .challenge}

> ## Comment Changes in GitHub
>
> The Collaborator has some questions about one line change made by the Owner and
> has some suggestions to propose.
>
> With GitHub, it is possible to comment the diff of a commit. Over the line of
> code to comment, a blue comment icon appears to open a comment window.
>
> The Collaborator posts its comments and suggestions using GitHub interface.
{: .challenge}

> ## Version History, Backup, and Version Control
>
> Some backup software can keep a history of the versions of your files. They also
> allows you to recover specific versions. How is this functionality different from version control?
> What are some of the benifits of using version control, Git and GitHub?
{: .challenge}
