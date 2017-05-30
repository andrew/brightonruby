# Can My Friends Come Too?

## Introduction

This is a talk about dependencies, their usage in the open source community and
some of the risks involved in relying on other people's software.

We're going to touch on a few key topics related to depending on other peoples software:

- Licensing
- Security
- Maintenance and Sustainability
- Risk

### Who am I?

My name is Andrew, for the past two and a half years I've been watching and recording
the activity of all of open source into a project called Libraries.io

### What is Libraries.io?

Libraries.io is an Open Source Discovery Service that helps you make more informed
decisions about the software you depend upon.

Libraries.io has three main aims:

- Discoverability - Helping developers make faster, more informed decisions about the software that they use.
- Maintainability - Helping maintainers understand more about the software they depend upon and the consumers of their software.
- Sustainability - Supporting undervalued software by highlighting shortfalls in contribution and funneling support to them.

It does this by monitoring the activity of 33 package managers, every new version
of every library that's published and their dependencies.

It also trawls every open source repository hosted on GitHub, GitLab and Bitbucket,
around 25 million at this point, and indexes the dependencies of each one, mapping
out a vast interconnected network all of open source.

It's a completely open source project, funded by Sloan and Ford Foundations with
the goal of raising the quality of all software.

### So what?

Having collected all of this, we can use this to analyze usage patterns and behaviors
within different communities. We can also find problems and weak points in the network
and provide data to help communities fix them and individuals or companies avoid
falling into the same traps.

## Depending on other peoples software

97% of companies use open source in some way (http://www.zdnet.com/article/its-an-open-source-world-78-percent-of-companies-run-open-source-software/)

Everyone is building on the shoulders of giants

Reduce duplicate work by sharing under license that allows reuse and modification

Accelerate the speed of development and allows you to focus on the unique challenges
of your project or business rather than reinventing the wheel time and again.

### Free as in Puppy

Open Source Software is often described as "Free as in Freedom", you are allowed to
read, share, modify and re-use the source code with little to no restrictions.

Most open source licenses include something along the lines of:

"THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE."

You don't download, or import, a software dependency, you adopt it. Like adopting
pets, it's a responsibility for the life of your product.

https://twitter.com/davecheney/status/616931340466786304

Some would say that makes it more like "Free as in Puppy", although you got it
for free, the puppy needs constant attention, feeding, watering and walking on
twice daily basis for 10 years plus, the total cost of ownership of the puppy
is anything but free.

### You're on your own

So the software is free but it's up to you to make sure that it's:

- correctly licensed
- free of security vulnerabilities
- actual works!

### Transitive dependencies

Often higher level libraries are built on top of other libraries, which in turn may
have their own dependencies, building up a tree of dependencies that your application
requires to function.

For example version 5.1.1 of the `rails` gem has 11 direct runtime dependencies
and 26 transitive, so installing one gem, results in 38 gems in total being installed.

You didn't explicitly request those extra dependencies, they just came along for the ride.

But those dependencies are now your problem too, that one free puppy brought 38
others along with it!

### Lockfiles

One other thing to bare in mind here is that for every new version of one of those
dependencies, there could be new dependencies added to the or swapped out.

One of the key features of Bundler is the Gemfile.lock file, which allows a developer
to reproduce the exact transitive dependency tree the way it was last successfully
installed as.

This means the developer chooses when to add, update or change dependencies rather
than getting a new selection of things every time you install the dependencies.

We take this for granted now in the ruby world but for many other package managers
this isn't the default behavior, opening you up to whole other worlds of dependency hell.

**** puppy break ****

So let's look at some of the issues that all these puppies can bring to your ruby projects:

## Licensing

### Unlicensed code
### Copyleft licenses
### Conflicting licenses
### Transitive licenses
### Non-Open Source Licenses (example: greensock-rails)


## Security

### CVEs
### Ruby Advisory Database
### Native dependencies
### Typosquatting - http://incolumitas.com/2016/06/08/typosquatting-package-managers/
### Worms - https://www.infoq.com/news/2016/03/npm-infection

## Maintenance and Sustainability

Software being "Done" is like lawn being "Mowed".

https://twitter.com/ourfounder/status/770075137332932608

Software being "Done" is like poodle being "Groomed".

https://www.instagram.com/p/BJnGuWXjGCj


- Deprecated libraries
- Unmaintained libraries
- Dead libraries
- Unresponsive issue trackers
- Deleted/removed code

### Digital Infrastructure

Shared, public code makes up the digital infrastructure of our society today. In
the face of unprecedented demand, the costs of not supporting our digital
infrastructure are numerous. No individual company or organization is
incentivized to address the public good problem alone. In order to support our
digital infrastructure, we must find ways to work together.

### Bus Factor

- code contributors
- package manager owners

## Frontend dependencies

all the same thigns for npm

## System dependencies

All the same things but for System dependencies

## Risk

unmaintained projects
public facing
personal data


## mitigation

lockfile
vendoring
automatic updating

## Conclusion
