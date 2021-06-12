# Bringing Pinax Back to Life- PyCon US Maintainers Summit Talk

## Table of Contents

- [About](#about)
- [Slides and Script Table of Contents](#slides-and-script-table-of-contents)
- [Slides and Script](#slides-and-script)   
- [Attribution](#attribution)
- [Contact Kati](#contact-kati)
- [Copyright](#copyright)

<hr>

## About

Slides and script for a pre-recorded talk Katherine "Kati" Michel ([Twitter](https://twitter.com/KatiMichel), [GitHub](https://github.com/KatherineMichel)) gave at PyCon US 2021 [Maintainers Summit](https://us.pycon.org/2021/summits/maintainers/), published Monday, May 10, 2021.
 
Slide Deck
* [Original slide deck](https://docs.google.com/presentation/d/16oi3jpggHZ0L_rKWlqRGh3BzHmi6wzkd-DWvbVTedsY/edit?usp=sharing)

Video
* [Video recording](https://youtu.be/KfPukNq7lVI)

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Slides and Script Table of Contents

- [Bringing Pinax Back to Life](#bringing-pinax-back-to-life)
- [About Me](#about-me)
- [In Summary](#in-summary)
- [Time Machine](#time-machine)
- [Time Machine: 2008](#time-machine-2008)
- [How It Began](#how-it-began)
- [Fast Forward: 2017](#fast-forward-2017)
- [How It Was Going](#how-it-was-going)
- [How It Was Going, 80 Project and Apps](#how-it-was-going-80-project-and-apps)
- [How It Was Going, GitHub Organization, Global Docs, and Slack](#how-it-was-going-github-organization-global-docs-and-slack)
- [How It Was Going, Sustainability Lacking](#how-it-was-going-sustainability-lacking)
- [Simplified, Self-Service, and Self-Sustaining](#simplified-self-service-and-self-sustaining)
- [Tribal Knowledge](#tribal-knowledge)
- [GitHub Open Source Survey](#github-open-source-survey)
- [Pinax Documentation](#pinax-documentation)
- [Documentation](#documentation)
- [One Source of Docs](#one-source-of-docs)
- [Variations in Configurations](#variations-in-configurations)
- [One Configuration Approach](#one-configuration-approach)
- [Reduce the Backlog](#reduce-the-backlog)
- [Engagement with Individuals](#engagement-with-individuals)
- [Communicate Better](#communicate-better)
- [Engagement with Community](#engagement-with-community)
- [Automation](#automation)
- [How It's Going: July 2020 Release](#how-its-going-july-2020-release)
- [How It's Going: 21.05 Release](#how-its-going-2105-release)
- [Biggest Lesson Learned](#biggest-lesson-learned)
- [Additional Ideas](#additional-ideas)
- [Challenge and Opportunity](#challenge-and-opportunity)
- [Thank You](#thank-you)

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Slides and Script

The script is a general outline and varies somewhat from what was said during the talk.

<table>

<tr><td width="30%">

![Slide 1](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_0.jpg)

</td><td>

### Bringing Pinax Back to Life

* Hi everyone
* It’s great to be here
* My name is Katherine Michel. I also go by Kati
* My talk is called “Bringing Pinax Back to Life”

</td></tr>


<table>

<tr><td width="30%">

![Slide 2](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_1.jpg)

</td><td>

### About Me 

* A little bit about me
* I’m a Consultant to the Wharton School at the University of Pennsylvania
* I work on a project called Simpl… it’s an open-source Python/Django/React game simulation framework 
* Stanford Code in Place Section Leader
* Pinax Maintainer/Web Developer
* DEFNA (Django Events Foundation North America) Board Member 
* At DEFNA we oversee the high level details of DjangoCon US and Django outreach across North America
* DjangoCon US Website Co-Chair

</td></tr>


<table>

<tr><td width="30%">

![Slide 3](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_2.jpg)

</td><td>

### In Summary

* My talk is about Pinax
* Pinax is an open-source library of reusable Django starter projects, apps, and themes for building websites. When developers began building Pinax in 2007, they had fun adding to it, but eventually Pinax had grown to be around 80 projects and apps. 
* There was not a strategy in place to make Pinax as easy as possible to maintain. So the maintainers began to suffer burnout. 
* I was hired to work on Pinax in the fall of 2017. In my talk, I'll outline the critical problems I discovered and the solutions I've implemented to make Pinax healthier and easier to maintain so that maintainers can get more done and contributors can be more easily onboarded. 

</td></tr>


<table>

<tr><td width="30%">

![Slide 4](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_3.jpg)

</td><td>

### Time Machine

* To better understand this story, we need to go back in time to 2008

</td></tr>


<table>

<tr><td width="30%">

![Slide 5](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_4.jpg)

</td><td>

### Time Machine: 2008

* Some Django enthusiasts had formed a group called the “Hot Club of France,” named after Django Reinhardt’s band. 
* They had found themselves reusing some of the same code patterns while building websites with Django
* At the first ever DjangoCon US, James Tauber, one of the original Pinax authors, gave a talk about this new community called Pinax

</td></tr>


<table>

<tr><td width="30%">

![Slide 6](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_5.jpg)

</td><td>

### How It Began

* James talked about his own site Quisition
* Even though it was a flashcard site, much of its functionality had nothing to do with flashcards
* The “Hotclub of France” members had begun to abstract these patterns into reusable starter projects, apps, and themes
* As web technologists, they wanted to create a reusable Django library that would make choices and compromises
* This would enable them, as website creators, to focus on the features at the top of the stack
* Then they could go from website idea to realization more quickly

</td></tr>


<table>

<tr><td width="30%">

![Slide 7](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_6.jpg)

</td><td>

### Fast Forward: 2017

* Let’s fast forward to 2017
* It had been around 10 years since the Pinax idea had been born
* I was hired to work on Pinax

</td></tr>


<table>

<tr><td width="30%">

![Slide 8](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_7.jpg)

</td><td>

### How It Was Going

* So what was the state of Pinax by now?
* It’s quite common, from the very beginning until now, for people to discover Pinax and say “it’s everything they ever dreamed of”
* On this slide is one of the very early tweets about Pinax… someone says “Pinax is every idea I’ve ever had.”

</td></tr>


<table>

<tr><td width="30%">

![Slide 9](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_8.jpg)

</td><td>

### How It Was Going, 80 Project and Apps

* By 2017, Pinax had grown to be a large group of professional-quality, interdependent Django projects and apps
* This included starter projects with Pinax apps pre-installed and a command line interface to install them
* This also includes sophisticated testing, packaging, and continuous integration configurations
* The Pinax GitHub organization alone has around 80 repos in it
* This slide includes many of the more popular ones

</td></tr>


<table>

<tr><td width="30%">

![Slide 10](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_9.jpg)

</td><td>

### How It Was Going, GitHub Organization, Global Docs, and Slack

* In addition to the GitHub organization
* Pinax now had a global docs site and a Pinax Slack channel for community and support
* There are also app-specific docs in individual repos

</td></tr>


<table>

<tr><td width="30%">

![Slide 11](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_10.jpg)

</td><td>

### How It Was Going, Sustainability Lacking

* But… 
* Without a strategy in place to make Pinax as easy as possible to maintain, the maintainers began to suffer burnout. 
* By now, many of the original authors had moved on
* Sustainability was lacking

</td></tr>


<table>

<tr><td width="30%">

![Slide 12](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_11.jpg)

</td><td>

### Simplified, Self-Service, and Self-Sustaining

* The goal in general of my work has been to work to make things simpler and self-service
* As a result, newcomers, contributors, and maintainers could help themselves
* And therefore, create a culture that could sustain itself

</td></tr>


<table>

<tr><td width="30%">

![Slide 13](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_12.jpg)

</td><td>

### Tribal Knowledge

* Problem: Tribal knowledge
* Solution: Document the tribal knowledge
* The Pinax authors knew how to do things quickly, but the knowledge remained in their heads
* In fairness, they were often busy and working quickly to meet deadlines
* But… the barrier of entry knowledge-wise was fairly high and the docs were sparse and not beginner friendly

</td></tr>


<table>

<tr><td width="30%">

![Slide 14](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_13.jpg)

</td><td>

### GitHub Open Source Survey

* GitHub did an open source survey in 2017 and they found that documentation is...
* Highly valued
* Often overlooked
* And a means for establishing inclusive and accessible communities

</td></tr>


<table>

<tr><td width="30%">

![Slide 15](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_14.jpg)

</td><td>

### Pinax Documentation

* For a while, my time was spent just figuring out how things had been done
* Then I began to document it… 
* I started by creating a release plan that explained the “Pinax way of doing things”
* Then moved on to creating a global community health file repo filled with default files
* This included a Code of Conduct
* A community plan
* Contributing and support information
* Information for Maintainers
* And issue and PR templates

</td></tr>


<table>

<tr><td width="30%">

![Slide 16](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_15.jpg)

</td><td>

### Documentation

* Problem: Existing docs difficult to find, duplicated, and inconsistent
* Solution: One source of documentation, easy to find, and use
* There was some documentation already in existence
* But it had been created ad hoc over the years
* There were bits of documentation here and there, some forgotten, some private

</td></tr>


<table>

<tr><td width="30%">

![Slide 17](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_16.jpg)

</td><td>

### One Source of Docs

* Pinax has a wiki
* I organized these historical docs, links, and new release plans in a Pinax wiki
* Then a blurb was added to the repo READMEs to make all of the docs more discoverable
* Including the global docs, app specific docs, tagged and published releases, support, contributing, and release docs
* Including the global docs, wiki, community health files, app specific docs, tagged and published releases, and support, contributing, and release docs
* This goes back to the DRY (Don’t repeat yourself principle)... one source of truth

</td></tr>


<table>

<tr><td width="30%">

![Slide 18](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_17.jpg)

</td><td>

### Variations in Configurations

* Problem: Variation in configurations
* Solution: Choose one configuration approach and implement across projects
* A number of people had created and worked on different Pinax projects at different times
* Because of this, there was a lot of variation in terms of how things had been done
* I can tell you from personal experience that as a newcomer, this made the code collectively harder to understand and more difficult to maintain

</td></tr>


<table>

<tr><td width="30%">

![Slide 19](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_18.jpg)

</td><td>

### One Configuration Approach

* After some research, I chose one configuration approach and implemented it across repos 
* I also detailed it in the release plan
* The more consistent the GitHub organization is, the better

</td></tr>


<table>

<tr><td width="30%">

![Slide 20](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_19.jpg)

</td><td>

### Reduce the Backlog

* Problem: Lack of engagement with individuals
* Solution: Reduce backlog of issues and PRs and catch up with engagement

</td></tr>


<table>

<tr><td width="30%">

![Slide 21](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_20.jpg)

</td><td>

### Engagement with Individuals

* Between releases
* Over 160 issues closed
* Over 100 PRs merged
* Over 30 PRs closed
* Countless questions answered in issues and Slack
* This was quite difficult at times, because many of the issues and PRs were the more difficult ones left outstanding
* I began with resolving the lowest hanging fruit issues and PRs knowledge-wise and working my way up
* The idea was to reduce the number until the new and existing issues and PRs would be more manageable

</td></tr>


<table>

<tr><td width="30%">

![Slide 22](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_21.jpg)

</td><td>

### Communicate Better

* Problem: Lack of engagement with the community
* Solution: Write more blog posts about plans and progress, and publicize well

</td></tr>


<table>

<tr><td width="30%">

![Slide 23](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_22.jpg)

</td><td>

### Engagement with Community

* I began to write blog posts and tweet about them
* The posts might be about Pinax, or some other Django-related activity and I would mention Pinax
* People began to become interested in Pinax, telling me that they had heard about Pinax through my writing
* It can have a huge benefit to stop and take time to write about the accomplishments and progress of the project and share it with the community 
* Even if a handful, or even one person, becomes interested and contributes, it can make a major impact
* It can also make people aware of the project and gives them social proof that it’s actively being maintained

</td></tr>


<table>

<tr><td width="30%">

![Slide 24](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_23.jpg)

</td><td>

### Automation

* Problem: Tasks being done manually
* Solution: Automate tasks
* Automating tasks lowers the risk of burnout

</td></tr>


<table>

<tr><td width="30%">

![Slide 25](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_24.jpg)

</td><td>

### How It's Going: July 2020 Release

* In July 2020, based on what I had learned,I oversaw the completion of an important Pinax release. 
* Around 28 apps were included and we notably dropped support for Python 2.7
* It was a huge milestone for me, personally and professionally. Not only did I initiate the release, but I managed the end-to-end process. I created the release plan, oversaw the work of others, updated 10 apps myself, merged all of the PRs, and tagged and published the packages. 

</td></tr>


<table>

<tr><td width="30%">

![Slide 26](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_25.jpg)

</td><td>

### How It's Going: 21.05 Release

* Pinax is a work in progress and has a lot of room still for improvement
* It doesn’t have a sense of community at the moment
* It’s time to update the Python/Django test matrix
* Automation that was not implemented in the last release can be implemented now
* Automation will be implemented (run tox from GitHub Actions, auto-publish to PyPI upon tagging)
* The global documentation should be improved
* Among other things...

</td></tr>


<table>

<tr><td width="30%">

![Slide 27](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_26.jpg)

</td><td>

### Biggest Lesson Learned

* The biggest lesson I’ve learned while working on Pinax is that the latest release succeeded because of my communication and teaching skills
* I learned this by accident
* My blog posts attracted contributors
* The release could not have been completed without the help of these contributors… it would have been too much work and required specialized skill
* The release documentation I had written enabled the contributors to help, to mutual benefit
* I was thrilled that they were able to use this documentation to complete a large portion of the work, with occasional support from me
* This assistance lives in with the next release

</td></tr>


<table>

<tr><td width="30%">

![Slide 28](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_27.jpg)

</td><td>

### Additional Ideas

* If you want more ideas, I recommend checking out the GitHub docs for the latest features available
* Bring on additional maintainers: selective permissions
* Workflow: protect branches, status checks, require review
* Automation: GitHub Actions/Apps, Probot
* Reduce scope: archive repos, mark repos as deprecated, disable issues
* Productivity: GitHub built in functionality (canned responses, notifications management, etc.)

</td></tr>


<table>

<tr><td width="30%">

![Slide 29](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_28.jpg)

</td><td>

### Challenge and Opportunity

* In closing...
* Pinax has created both fun and frustration
* But I’m personally grateful to have found a project like this to work on
* By having the freedom to grapple with Pinax, I’ve been able to develop professionally and improve Pinax in the process
* I’ve also been take what I’ve learned from Pinax and immediately apply it to other open source situations of any size
* I hope you’ve learned something today too. 

</td></tr>


<table>

<tr><td width="30%">

![Slide 30](https://speakerd.s3.amazonaws.com/presentations/55d27208aab64c78b8b07a8acb9e8bc8/slide_29.jpg)

</td><td>

### Thank You

* Feel free to contact me
* Twitter: KatiMichel
* GitHub: KatherineMichel
* Email: kthrnmichel@gmail.com

</td></tr>

</table>

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Attribution

The style of this transcript is heavily inspired by:

* Ana Balica's ([Twitter](https://twitter.com/anabalica), [GitHub](https://github.com/ana-balica)) transcript of her [Humanizing among coders](https://ana-balica.github.io/2017/05/28/humanizing-among-coders/) keynote for [PyCon CZ 2016](https://cz.pycon.org/2016). 
* Honza Javorek's ([Twitter](https://twitter.com/honzajavorek), [GitHub](https://github.com/honzajavorek)) transcript of Anna Ossowski's ([Twitter](https://twitter.com/OssAnna16), [GitHub](https://github.com/OssAnna16)) keynote [Be(Come) A Mentor! Help Others Succeed!](https://github.com/honzajavorek/become-mentor) for [PyCon CZ 2017](https://cz.pycon.org/2017/). 

Thank you!

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Contact Kati

* Email: kthrnmichel@gmail.com
* GitHub: https://github.com/KatherineMichel
* Twitter: https://twitter.com/KatiMichel

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Copyright

© 2021 to Present Katherine Michel. All Rights Reserved.
