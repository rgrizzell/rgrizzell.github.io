# Something of a Portfolio: Genesis

It would be a lie to say I hadn't thought about doing something like this for years. The appeal of having an online
portfolio was strong. One that can act as both a medium of expression and a demonstration of my skills. I didn't have
much of an idea of what that might look like. At first, it did what I was familiar with. I invested heavily in building
out a homelab. I hoped that talking about my learning experiences would be enough.

It ended up a great learning experience, but it what it lacked was demonstration. Getting to the interview and having
to pass around my phone with pictures? Sure, that might work just fine for the vast majority of folks. However, how do
they tell if it's all just talk of a big game? I felt that to some degree the folks on the other side of the table still
had to take my word for it. While my homelab still acts as a great tool for my professional development, it's also hard
to convey to non-technical folks what the significance of it is.

Hoping to have something better to show folks, I set upon my GitHub profile with renewed interest. It started as simply
writing Markdown files with the steps to replicate the homelab should something disastrous happen. It soon evolved into
a few other projects, but none I felt comfortable publishing due to the sensitive nature of the infrastructure it was
for. With few projects to show for, I wanted to improve the value of these learning experiences by sharing them with
others.

Around the middle of the COVID-19 pandemic, the OS on my workstation needed to be re-installed. My custom configs,
workspaces, and scripts were gone. I lost everything that wasn't saved in a Git repository. Vowing never to allow such
an egregious event to happen again, I took inspiration from the event to create a 
[dotfiles](https://github.com/rgrizzell/dotfiles) repository. I could be up and running in a matter of minutes rather a
day. All well and good, but managing credentials was still pain.

I stumbled across the answer in [drduh/YubiKey-Guide](https://github.com/drduh/YubiKey-Guide). It's a well put together
document that details the steps on turning most YubiKeys into physical representation of a GPG private key. This
partnered with a new interest in Cryptocurrency, devolved into a rabbit hole where I went through the effort of securing
the integrity of my identity and my work. An experience worthy of its own post. 

With a much better appreciation for the term DevSecOps, I realized that whatever my portfolio was going to be, it had to
be a demonstration of those three key terms. Development, Security, and Operations. I had to develop it myself, using
security best practice, and make sure it was resilient.


# It Starts with a Set of Goals

The goals are to develop a modern, responsive site that can:
- Act as my professional homepage.
- Provide a copy of my resume and relevant work.
- Render blog posts and technical documentation.
- Be cryptographically verifiable.
- Run independently of my infrastructure.

The first real steps after defining a set of broad goals was to earmark some pages in my Field Notes booklet. I'll be
using pages to sketch out the UI and organize thoughts about how certain components behave. I think more professional
designers may choose to use software for this, but for me, it always seems to start with a writing utensil. The Field
Notes books are a solid option, especially in more rugged work environments. For now, it's just handling my rugged
handwriting.

![Field Notes Booklet with Graph Paper](img/notebook.jpg)

Getting the Git repository created was the next step. Regardless of the software being used, having it stored in a
public repository is a must. It was also equally important that I signed each commit with my GPG key. Auto-signing was
enabled immediately put to use by rebasing everything into the root commit and signing it.

```shell
git config commit.gpgSign true
git rebase -i --root
```

With both items addressed and ready to do, attention shifted into the research phase.

## Research

Given my lack of experience with Frontend Development, I felt it was necessary to consult the internet for online
courses. I ended up settling on Codecademy to provide the fundamentals necessary for understand the majority of the
resources elsewhere.

I