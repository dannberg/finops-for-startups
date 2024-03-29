[![Netlify Status](https://api.netlify.com/api/v1/badges/869aff8b-c740-418f-9358-a8024a2e5913/deploy-status)](https://app.netlify.com/sites/finopsforstartups/deploys)
# Welcome to FinOps for Startups

_[FinOps for Startups](https://finopsforstartups.com)_ is an upcoming book by [Dann Berg](https://dannb.org). This Github repo, and public-facing [website](https://finopsforstartups.com), is my collection of research for this book.

What is FinOps? As defined by the FinOps Foundation:

> FinOps is an operational framework and cultural practice which maximizes the business value of cloud, enables timely data-driven decision making, and creates financial accountability through collaboration between engineering, finance, and business teams.

In more basic terms, FinOps is:

- the bridge between engineering and finance
- a set of best practices to foster a culture of cloud cost mindfulness
- a collection of methods and practices to lower cloud bills

FinOps for Startups explores how this can be beneficial to early-stage companies, where growth is typically the highest priority, even over cost.

# Research in public

This Github repo and associated website is part of _another_ growing movement online. That movement goes by several names ("learning in public," "thinking in public," "doing in public," "building in public") but it's all pretty much the same thing.

It's about publishing _while_ you're working, making both the process and the content available for public consumption. This practice has several benefits:

- accountability
- enhanced critical thinking
- knowledge sharing
- transparency
- your audience gains a sense of ownership

While I am working on _FinOps for Startups_, I'm going to simultaneously **research in public**, by which I mean publish my notes on [finopsforstartups.com](https://finopsforstartups.com).

## About this site

This website is written and published using:

- [Obsidian](https://obsidian.md)
- [Quartz](https://quartz.jzhao.xyz)
- [Netlify](https://www.netlify.com/)

Obsidian is a markdown note taking application (which I use extensively, just [look at my blog](https://dannb.org/blog/)) and Quartz is a markdown-to-static-site generator purpose-built for Obsidian. Netlify is a simple and free static website host.

**Obsidian Setup**

- Theme: [AnuPpuccin](https://github.com/AnubisNekhet/AnuPpuccin) - Dark Mode
- Plugins:
	- [Templater](https://silentvoid13.github.io/Templater/introduction.html)
	- [Dataview](https://blacksmithgu.github.io/obsidian-dataview/) (internal use only, does not render in Quartz)

## Using this repo

This is my first time using Quartz, so this section of the README is just going to be some internal notes for me.

When running the command `git remote -v` we see that this repo is the origin, but `https://github.com/jackyzha0/quartz.git` is upstream for fetch and push. This shows the repo that this was forked from, and is a way to keep quartz updated.

Run the site locally:
```sh
npx quartz build --serve
```

Fetch the changes from the upstream repository (Quartz):
```sh
git fetch upstream
```

To push local changes to Github:
```sh
npx quartz sync
```

To sync remote changes (make sure your git it up-to-date):
```sh
npx quartz sync --pull
```

To pull all remote files to *replace local files* (**warning:** this you will *lose all local changes*):
```sh
git fetch origin
git reset --hard origin/v4
git clean -fd
```

^ This fetches the latest changes from remote, hard reset local brach to match remote, then cleans untracked files. The last two commands *result in the loss of local changes*. Make sure you want that.
### Setting up on a new computer
Currently using NPM version 10.2.4, so make sure to update to that version.

```sh
npm install -g npm@10.2.4
git clone https://github.com/dannberg/finops-for-startups.git
cd finops-for-startups
npm i
npx quartz sync --pull
```

## About Dann Berg

Want to learn more about the author? This repo README is the wrong place for that. Go to [dannb.org](https://dannb.org) instead. Oh, and sign up for my [free monthly newsletter](https://dannberg.substack.com). If you're reading these words, there's a high likelyhood that you'll also enjoy my newsletter.

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.

![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)

This project and its contents are licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/). This means you are free to:

- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially.

Under the following terms:

- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

**No additional restrictions** — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

Notices:

You do not have to comply with the license for elements of the material in the public domain or where your use is permitted by an applicable exception or limitation.

No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material.
