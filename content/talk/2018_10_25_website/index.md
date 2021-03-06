+++
title = "DIY: webpage!"
date = 2018-06-28T16:00:00+02:00  # Schedule page publish date.
draft = false

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
time_start = 2018-10-25T16:00:00+02:00
#time_end = 2018-09-05T17:38:30+02:00

#authors (can be left blank)
authors = ["[Bertrand THIERRY (CNRS/LJLL)](https://www.ljll.math.upmc.fr/bthierry)"]

# Abstract and optional shortened version.
abstract = ""
abstract_short = ""

# Name of event and optional event URL.
event = ""
event_url = ""

# Location of event.
location = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected talk? (true/false)
selected = false

# Projects (optional).
#   Associate this talk with one or more of your projects.
#   Simply enter your project's filename without extension.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
#   Otherwise, set `projects = []`.
tools = ["hugo-academic"]

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["webpage"]

# Links (optional).
url_pdf = ""
url_slides = "../../slides/hugo-academic"
url_video = ""
url_code = ""

# Does the content use math formatting?
math = false

# Does the content use source code highlighting?
highlight = true

+++

## Promises

Using the static web generator [Hugo](https://gohugo.io) and the wonderful theme [Hugo-Academic](https://github.com/gcushen/hugo-academic/), we promise to:

1. Build a professional webpage in less than 10 minuts that [looks like this](https://themes.gohugo.io/theme/academic/)
2. Do not write a single line of neither HTML nor CSS: only [Markdown](https://en.wikipedia.org/wiki/Markdown) which is very simple to learn!
3. That's already a lot

## Tools needed

1. [Optional but highly recommended] Git and a [Github]({{<ref "tools/github.md">}}) or [Gitlab(.com)]({{<ref "tools/gitlab.md">}}) (but not the local Gitlab!) account
2. A good text editor: we recommend [VSCode]({{<ref "tools/vscode.md" >}})
3. [Optionnal: to work locally] [Hugo](https://gohugo.io/getting-started/installing/)

## Let's do it!

### Build the basic webpage

All the stages are detailed on the [exhaustive documentation of Hugo Academic](https://sourcethemes.com/academic/docs/) but we do remind some of them here. We assume you have a Github account but it is the same if you own a Gitlab(.com) one:

1. Have Github/Gitlab.com account
2. Go to [Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart)
3. Allow Netlify to modify your github/gitlab account
4. Choose a repo name (*e.g* "webpage")

At this stage, you already have a basic but working  website. The URL is however UGLY:

1. In your Netlify account: `Settings` → `Domain managment`: Change the URL base name (*e.g* myname.netlify.com)
2. Check again on the new URL!

Every time you do a `push` to your remote Git reposity, Netlify will rebuild your website. In case the rebuild failed, you can access the log to correct the mistake. Rebuilding the website takes about 20seconds.

### Local version

You have to install Hugo on your computer (see above). We assume that you want your folder to be named `webpage`.

- Clone the repository

```bash
> git clone https://path_to_repo webpage
```
- In a terminal and **in the folder**, launch

```bash
> git submodule update --init --recursive
> hugo serve
```
- Launch your browser and go to  http://localhost:1313

### Update theme

```bash
> sh update_academic.sh
```

And do not forget to `commit` and `push` !

### Send modification to remote

- Ask Git to track new file :

```bash
> git add /path/to/newfile
```
- (Lazy version) Commit every changes in the track files

```bash
> git commit -a -m "Message of the commit"
```
- Push to the remote

```bash
> git push
```

Refresh your webpage, it should be actualized in the minut.

{{% alert warning %}}
Please, try to never `commit` a broken code, *i.e* a code that Hugo fails to build. Always check if everything is fine locally!
{{% /alert %}}

### `/config.toml`

This is the main config file: choose the options you want by filling the blanks spaces (quite intuitive)

### Add/Modify content...

For every operations of that kind, [we refer to the documentation](https://sourcethemes.com/academic/docs/).
