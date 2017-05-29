# Postmortem Templates

This is a collection of postmortem templates derived from various sources such as the [Site Reliability Engineering](https://landing.google.com/sre/) book, [The Practice of Cloud System Administration](http://the-cloud-book.com/) book and other online resources.

## Template List
* [Template from Site Reliability Engineering book](templates/postmortem-template-srebook.md)
* [Template from The Practice of Cloud System Administration book](templates/postmortem-template-thecloudbook.md)
* [Template from Google Developers Blog post](templates/postmortem-template-google-api-infra.md)

## Load templates automatically

It is possible to load the postmortem templates automatically without copy pasting from the files or manually writing the structure every time you want to author an incident report.

### Vim
You can add the following line into your `.vimrc` file:

    au BufNewFile postmortem-*.md 0r ~/postmortem-templates/templates/postmortem-template-srebook.md

### Emacs
You can add the following line into your `.emacs` file:

    (add-hook 'text-mode-hook (lambda () (when (and (string-prefix-p "postmortem-" (buffer-name)) (= (point-max) (point-min))) (insert-file-contents "~/postmortem-templates/templates/postmortem-template-srebook.md"))))


In both cases the filename pattern is `postmortem-*`. For example, if you create a file named `postmortem-api-outage-2017-05-29.md` it will load automatically the predefined template into that file. You can replace both the postmortem template and pattern to match your.

### Postmortem resources
* [A collection of post-mortems](https://github.com/danluu/post-mortems)
* [Blameless PostMortems and a Just Culture](https://codeascraft.com/2012/05/22/blameless-postmortems/)
* [A Tale of Postmortems](https://blog.box.com/blog/a-tale-of-postmortems/)
* [Building a Blameless Post-Mortem Culture with Jason Hand](http://runasradio.com/Shows/Show/486)
* [The infinite hows](https://www.oreilly.com/ideas/the-infinite-hows)
* [Failure is Always An Option: How a Blameless Culture Leads to Better Results](https://victorops.com/blog/blameless-culture/)
* [How to write an Incident Report / Postmortem](https://sysadmincasts.com/episodes/20-how-to-write-an-incident-report-postmortem)
* [SysAdvent - Day 1 - Why You Need a Postmortem Process](https://sysadvent.blogspot.com/2016/12/day-1-why-you-need-postmortem-process.html)
* [Etsy’s Debriefing Facilitation Guide for Blameless Postmortems](https://codeascraft.com/2016/11/17/debriefing-facilitation-guide/)
* [Writing Your First Postmortem](https://medium.com/production-ready/writing-your-first-postmortem-8053c678b90f)
* [Site Reliability Engineering resources](https://github.com/dastergon/awesome-sre)