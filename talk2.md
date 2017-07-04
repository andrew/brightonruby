# Can My Friends Come Too?

1. Introduction

This is a talk about dependencies, their usage in the open source community and
some of the risks involved in relying on other people's software.

2. About Me

I'm Andrew, long time rubyist, first time Brighton Ruby speaker

3. About Me continued

You might know me such projects as:

- Split
- 24 Pull Requests
- Octobox

More recently I've been working on Libraries.io, a project that indexes libraries
from 33 different package managers and the 25 million open source repositories that
list them as dependencies.

4. Introduction continued

Today we'll touch on a few key topics related to depending on other peoples software:

- Maintenance
- Security
- Licensing
- Sustainability

Ultimately what we're talking about are some of the hidden costs and risks involved in
depending upon other peoples open source code.

5. Dependencies

When I say "dependencies", I'm talking about any pieces of software that your
programs need to run successfully.

That includes libraries, frameworks, tools, databases, operating systems, web services and APIs

For now let's focus on Rubygems, which I'd guess most of you here use on a very
regular basis.

6. Open Source usage

According to a 2015 survey, 78% of companies said their software
created for customers was built on open source, nearly double
that of 2010.

Open source has become the default choice, everyone is building on the shoulders
of giants.

Open source has reduced duplicate work by sharing under license that allows reuse and
modification and accelerated the speed of development and allows you to focus on
the unique challenges of your project or business rather than reinventing the
wheel time and again.

6. Free as in puppies

Open Source Software is often described as "Free as in Freedom", you are allowed to
read, share, modify and re-use the source code with little to no restrictions.

You don't download, or import, a software dependency, you adopt it. Like adopting
pets, it's a responsibility for the life of your product.

https://twitter.com/davecheney/status/616931340466786304

Some would say that makes it more like "Free as in Puppy", although you got it
for free, the puppy needs constant attention, feeding, watering and walking on
twice daily basis for 10 years plus, the total cost of ownership of the puppy
is anything but free.

7. Transitive Dependencies

Often higher level libraries are built on top of other libraries, which in turn may
have their own dependencies, building up a tree of dependencies that your application
requires to function.

For example version 5.1.1 of the `rails` gem has 11 direct runtime dependencies
and 26 transitive, so installing one gem, results in 38 gems in total being installed.

You didn't explicitly request those extra dependencies, they just came along for the ride.

But those dependencies are now your problem too, that one free puppy brought 38
others along with it!

9. Evaluating Open Source

So now we get into the meat of the talk.

Let's go over some of the main things you should consider when deciding on which
dependencies you should adopt into your codebase.

- Maintenance
- Security
- Licensing
- Sustainability

8. Maintenance

Software being "Done" is like lawn being "Mowed".

https://twitter.com/ourfounder/status/770075137332932608

- Accepting contributions
- Update to date dependencies
- Releasing new versions
- Responsive to support requests
- Bus factor https://libraries.io/bus-factor
- Deprecation

9. Security

- CVEs
- Security policies and process
- Threat model
- Native dependencies
- https://github.com/rubysec/bundler-audit

10. Licensing

- Unlicensed
- Proprietary
- Copyleft
- Conflicting licenses
- https://github.com/pivotal/LicenseFinder

11. Sustainability

https://twitter.com/mperham/status/880835731874168832

- Funding model
- bystander effect
- open collective
- Project adoption
- unseen infrastructure https://libraries.io/unseen-infrastructure

13. Other kinds of dependencies

- Frontend dependencies
- System level dependencies
- Web services and APIs

14. Conclusion

- Review your dependencies on a regular basis
- Support projects you use
- Consider adopting
