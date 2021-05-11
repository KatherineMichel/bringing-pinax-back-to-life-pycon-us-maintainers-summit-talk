00:01
hi everyone
00:03
it's great to be speaking at the picon
00:06
u.s maintainer summit
00:08
my name is catherine michael my talk is
00:11
called bringing pinx back to life
00:14
a little bit about me i'm a consultant
00:17
to the wharton school
00:18
i work on a game simulation framework
00:21
project called simple
00:23
i'm a pinx maintainer and web developer
00:26
and
00:27
a defna board member
00:30
my talk is about pinx pinx is an open
00:33
source
00:33
library of reusable django starter
00:36
projects
00:38
apps and themes for building websites
00:40
when developers began
00:42
building pinx in 2007 they had
00:45
fun adding to it but eventually pin x
00:48
had grown to be around 80 projects and
00:50
apps
00:51
there was not a strategy in place to
00:53
make pinx as easy as possible to
00:56
maintain
00:57
so the maintainers began to suffer
00:59
burnout
01:00
i was hired to work on pinx in the fall
01:02
of 2017.
01:05
in my talk i'll outline the critical
01:07
problems i discovered and the solutions
01:10
i've
01:10
implemented to make help pinx healthier
01:13
and easier to maintain
01:15
to better understand this story we need
01:17
to go back in time to 2008.
01:20
some django enthusiasts had formed a
01:23
group called the hot club of france
01:25
named after django reinhardt's band they
01:28
had found themselves reusing some of the
01:30
same code patterns while building
01:32
websites with django
01:34
at the first ever djangocon us james
01:37
tauber one of the original pinx authors
01:40
gave a talk about this new community
01:42
called pinx
01:44
james talked about his own site quizzion
01:48
even though it was a flashcard site much
01:51
of its functionality had nothing to do
01:53
with flash
01:54
cards the hot club of france members had
01:57
begun to abstract these patterns
01:59
into reusable starter projects apps and
02:02
themes
02:03
as web technologists they wanted to
02:06
create a reusable django library that
02:09
would make
02:09
choices and compromises this would
02:12
enable them as website creators to
02:15
focus on the features at the top of the
02:17
stack
02:18
then in this way they could go from
02:20
website idea to realization more quickly
02:24
let's fast forward to 2017.
02:27
it had been around 10 years since the
02:29
pinx idea had been born
02:31
and i was hired to work on pinx so what
02:35
was the state
02:36
of pinux by now it's quite common
02:39
from the very beginning until now for
02:41
people to discover
02:43
pinx and say that it's everything
02:45
they've ever dreamed of
02:47
for example on this side is one on the
02:49
slide is one of the very early tweets
02:51
about pinx
02:52
someone says pinx is every idea i've
02:54
ever had
02:56
by 2017 pinx had grown to be
03:01
a large group of professional quality
03:04
interdependent django projects and apps
03:07
this included
03:08
starter projects with pinx apps
03:11
pre-installed and a command line
03:13
interface to install them
03:15
it also includes sophisticated testing
03:17
packaging
03:19
and continuous integration
03:20
configurations
03:22
the pinx github organization alone
03:25
now has around 80 repos in it this slide
03:28
includes many of the more popular ones
03:32
in addition to the github organization
03:34
pinx now has a global docs site
03:37
and a pinx slack channel for community
03:40
and support
03:41
and there are also app specific docs and
03:43
individual
03:44
repos but without a strategy in place to
03:48
make pinx as
03:50
easy as possible to maintain the
03:52
maintainers had begun to suffer burn
03:54
out and by now many of the original
03:57
authors had moved on
03:58
so sustainability was lacking
04:02
the goal of my work in general has been
04:05
to
04:05
make things simpler in self-service as a
04:08
result
04:09
newcomers contributors and maintainers
04:12
can
04:12
could help themselves and ideally
04:15
therefore
04:16
create a culture that could sustain
04:18
itself
04:19
the first problem i came upon was tribal
04:22
knowledge and the solution was to
04:24
document the tribal knowledge
04:26
the pinx authors knew how to do things
04:29
quickly but the knowledge remained in
04:30
their heads
04:31
and so the barrier of entry knowledge
04:34
wise was fairly high
04:36
but the docs were sparse and not
04:38
beginner friendly
04:40
github did an open open source survey in
04:43
2017
04:44
and they found that documentation is
04:46
highly valued
04:47
often overlooked and a means for
04:50
establishing inclusive and accessible
04:52
communities
04:54
for a while i spent my time figuring out
04:56
how things were done
04:57
i started by creating a release plan
05:00
that explained the pinx way of doing
05:02
things then moved on to creating
05:05
a global community health file repo
05:07
filled with default files including
05:10
a code of conduct a community plan
05:13
contributing and support information
05:15
information for maintainers
05:18
and issuing pr templates the next
05:21
problem was that the existing docs were
05:23
difficult to find
05:25
duplicated and inconsistent and the
05:28
solution was to create
05:30
one source of documentation that would
05:32
be easy to find
05:33
and use there were bits of documentation
05:37
here
05:37
and there some forgotten and some pro
05:40
private pinx has has a wiki so i
05:43
organized the historical docs links and
05:46
new release plans
05:47
in the wiki and added a blurb to the top
05:50
of the repo readmes to make
05:52
all of the docs more discoverable
05:53
including global docs app specific docs
05:57
tagged and published releases support
05:59
and contributing
06:01
information and release docs the next
06:04
problem was a variation in
06:05
configurations and the solution was to
06:08
choose one
06:09
configuration approach and implement it
06:11
across projects
06:12
a number of people had created and
06:15
worked on different
06:16
pinx projects at different times and
06:18
because of this there was
06:20
a lot of variation in terms of how
06:22
things had been done
06:23
and i can tell you from personal
06:25
experience as a as a newcomer that that
06:27
can make it harder
06:29
to understand the code so after some
06:32
research i chose one configuration
06:35
approach and implemented it across repos
06:38
and detailed this in the release plan
06:42
the next problem was a lack of
06:43
engagement with individuals and the
06:46
solution was to reduce the backlog of
06:48
issues and prs and catch up with
06:50
engagement
06:51
between releases over 160 issues were
06:55
closed
06:56
100 prs merged 30 prs closed and
06:59
countless
07:00
questions answered in issues in slack
07:03
i began by resolving the lowest hanging
07:06
fruit issues and prs knowledge wise and
07:08
working my way up
07:10
and the idea was to reduce the number
07:12
until the newing
07:13
existing issues in prs would be more
07:15
manageable
07:17
the next problem was a lack of
07:18
engagement with the community and the
07:20
solution was to write more blog posts
07:23
about
07:24
plans and progress and publicize them
07:26
well
07:27
i started writing blog posts and
07:29
tweeting about them and the post might
07:31
be about pinx or some other django
07:33
related activity and i would mention
07:35
pinx
07:36
and people began to be interested in
07:38
pinx
07:39
telling me that they had heard about it
07:41
through my writing
07:43
and i realized that that it could have a
07:45
huge benefit to stop and take time to
07:47
write about
07:48
the accomplishments uh and progress of
07:50
the project
07:51
and share it even if a handful or
07:55
one person becomes interested and
07:56
contributes it can have a huge impact
08:01
the last problem was the tasks were
08:03
being done
08:04
done manually and the solution was to
08:06
automate the tasks to
08:08
lower the risk of burnout so how's it
08:12
going
08:13
in july of 2020 i oversaw the completion
08:16
of an
08:17
important pinx release around 28 apps
08:20
were included and we
08:21
notably dropped support for python 2.7
08:24
it was a huge milestone for me
08:26
personally and professionally because i
08:28
was able to
08:29
oversee the entire into in process
08:33
but pinx is a work in progress and
08:35
there's still room for improvement
08:37
we don't have a sense of community that
08:39
we could have at the moment but
08:41
i'm happy to say that we're moving
08:43
forward with a 21.05 release
08:46
to update the python django test matrix
08:50
and implement some of the automation
08:52
that we didn't get to with the last
08:54
release such as running talks from
08:56
github actions and
08:58
implementing auto publish to pi p i upon
09:01
tagging
09:02
and the global documentation needs to be
09:05
improved
09:06
so the biggest lesson i've learned in
09:08
all of this that i want to impart to you
09:12
is that the last release succeeded
09:15
because of my communication
09:16
and teaching skills which i sort of
09:18
learned by accident
09:20
when my blog posts attracted
09:22
contributors i
09:24
received some help that enabled the
09:27
release to be completed
09:29
i it wouldn't have been done without the
09:32
help of
09:32
the contributors who came along the
09:35
release documentation i had written
09:37
enabled people to contribute on their
09:40
own with minimal help from me
09:43
so if you want more ideas about ways to
09:47
make
09:47
maintain maintaining an open source
09:50
project easier
09:52
i've included a slide with additional
09:54
ideas
09:55
in my slide deck and i just want to say
09:59
that even though pinx has been fun and
10:01
frustrating
10:02
i'm personally grateful to have had the
10:04
experience of working on it because i've
10:06
learned a lot
10:08
if you have any questions feel free to
10:10
contact me thank you
