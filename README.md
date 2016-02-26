# Contributing to the Puppet Community

## Ways to Contribute

* Puppet Core
* Puppet Modules
* Documentation
* Filing Tickets
* Answering Questions on IRC/Mailing Lists
* Hackathons
* Triages
* ask.puppetlabs.com

## Code Contributions

### Puppet Core

Core puppet has quite a few open source components that anyone can contribute to. In addition to puppet, projects
like facter, hiera, marionette-collective, puppet-server, puppet-db and many more are great places to contribute. Developing
on core components (unlike when contributing to modules) may require you to know a language beyond Ruby or Puppet
as some of our projects are written in other languages such as C++ and Clojure.

### Puppet Modules

### Work Flow

1. **Figure out what you want to work on.** There is endless work to be done against puppet core and modules. If you have
a problem or feature that you think you want to work on, the first step is to make sure there's a ticket for that work.
Go to [tickets.puppetlabs.com](https://tickets.puppetlabs.com/) and do a quick search to see if a ticket describing the
work you want to do already exists. All core projects will have their own Jira project (e.g. PUP for puppet, FACT for facter)
and there is a MODULES project for modules work. If there is a ticket, great! Reference that one. If not please create one.
Browsing tickets is another great way to find an idea if you don't already have something in mind.

2. **Sign the CLA** (if you're working on core projects). If you want to contribute to puppet core, you'll have to sign
the [Contributor's License Agreement](https://cla.puppetlabs.com). This basically just says "hey it's okay if you want
to use my code in your project". This is not needed for contributing to modules.

3. **Clone and fork the repository**. Once you know what you want to work on, it's time to grab some code. All the projects
live on GitHub under the [puppetlabs](https://github.com/puppetlabs) GitHub organization. Find the repo for the project
you're working on, for example [puppetlabs/puppet](https://github.com/puppetlabs/puppet) or
[puppetlabs/puppetlabs-apache](https://github.com/puppetlabs/puppetlabs-apache). Then create a fork of the repository
and clone it locally so you can get started. If you need more help on git and git work flows, check out the Resources
section.

4. **Create a topic branch.** We prefer to merge pull requests from topic branch to master rather than master to master.
Please create a git topic branch where you can do your work.

5. **Make your changes.** Make the fix or add the feature you want to add. Please make sure to follow the
[contributing guidelines](https://github.com/puppetlabs/puppet/blob/master/CONTRIBUTING.md) and commit as you go using
correctly formatted commit messages. You can find resources for help learning the programming language you need to use
and should absolutely ask for help on IRC if you're feeling stuck. Our community is full of helpful friendly people
who would love to answer your questions.

6. **Run and write tests** as appropriate. Most of our project will have a built in tests suit to catch regressions. As
you make your changes, please run spec tests to make sure something hasn't been accidentally broken. Most of our
repositories will run tests automatically when a pull request is submitted. If tests are failing we will likely kick
the pull request back to you, so to speed up the process please run tests on your own.  In many situations
you will also need to update tests or even write new ones. Tests can often be even trickier than fixing the code,
so again please reach out if you're stuck.

7. **Open a pull request.** Once your work and your tests are ready to go it's time to open a pull request! Please
take a second to double check that your work follows the contributing guidelines and then open a pull request
targeting the master branch. Always target master unless it's a special case and you've spoken with someone
who has told you which branch to target.

8. **Be ready for feedback and discussion.** Once your pull request is in you're not really done, you've just entered the
next phase in the process. Many people think that once they open a pull request they're done, but in almost all cases
we'll have feedback, questions, or changes we'd like you to make. Please keep an eye on the pull request or your GitHub
notifications so you're ready to respond to feedback. That way we can get your code reviewed and merged must faster.

### Tips and Tricks

  * **Reach out to the community.** All and all, puppet has a pretty cool community made up of people who are kind and
  passionate about the work they do. Don't be afraid to reach out and ask for help or advice, chances are there's someone
  who's more than willing to answer your questions. We have a lot of ways you can talk to folks in the puppet community,
  and all of those resources are monitored by both people in and outside of Puppet Labs. Reference the "Getting Help"
  section below for a complete list.
  * **Ask good questions.** When you're asking questions, there are a lot of people who want to help you out, so make
  it easy for them to do so. Make sure you ask your questions are asked in the right forum and that you include the
  information that people need to help out. If you're not sure where the right place to ask your question is, check out
  the "Getting Help" section for a break down of IRC vs Google Groups etc. If you're looking for tips on how to ask questions,
  take a look at the "Asking Good Questions" section below.
  * **Start small.** Puppet can be scary, anyone who's worked on it before will agree with that. The last thing you want
  is to take on a task that's too big and get discouraged, so make sure that you pick something that's appropriate for your
  skill level. Try to find an area you're already somewhat familiar with, like maybe an operating system that you work with,
  and pick a bug or feature that's manageable in size and scope. The less source code files you can touch the better. Then,
  as you start to get comfortable with the little tasks, you can move on to your bigger grander ideas.
  * **Don't be discouraged by mistakes.** Programming is tough, and when you're learning the ropes it can be challenging.
  It's really important to keep in mind that making mistakes and failing is an essential part of the process when you're
  learning something new, so frame your mistakes as a chance to learn instead of a reason to quit. In most cases, we'll
  have suggestions or changes we'd like you to make when you submit a pull request, so don't be discouraged if we leave
  a lot of comments. It's our way of helping you be the best contributor you can be, and make sure your contribution is
  maintainable. So try to be opened minded and receptive to feedback, and remember that every mistake is a chance to learn
  something new.
  * **Please bother us if you don't hear back.** We're pretty busy people, and for most of us we have a lot to do in
  addition to working with the community. If you haven't heard from us, it's definitely not because we don't care about
  you or your work, it's because somethings just fall off the radar no matter how hard we work to keep track of everything.
  So please, if you haven't heard back, ping us again. Comment on your pull request or ask on IRC to gently remind us
  to take a look.
  * **Make sure your patch is being submitted to the right place.** Puppet is a pretty big and distributed tool, it lives
  in a lot of different places. The first question you want to ask yourself is if your patch belongs in core puppet itself
  (puppet, fact, hiera, etc) or if it belongs in a module. Every situation is different, but a good rule of thumb is that
  if you're changing existing behavior in puppet (like fixing a bug or making an improvement) it should go in puppet. However
  if you're adding a big new feature, chances are it might belong in a module. The question you need to answer then is if
  it should be in an existing module or a new one. Do a quick search of the forge and see if if there's already a module
  related to what you want to do, then take a look and see if you think your feature would fit in. If not, you may want
  to write your own module.
  * **Update tests and documentation as appropriate.** In order to make sure our software is maintainable, we have test
  and documentation. When you're developing, you want to make sure you regularly run our suit of unit tests to see if
  anything was broken. Chances are, you may need to update a test or even add a new one with your pull request. We know
  this can be really tough, and we often help out with this, so if you need help please ask. You don't want tests to be
  what prevents you from submitting your contribution, but it's essential that they're up to date. **TODO:** How do you
  update docs??

### Resources

  * Ruby
  * Rspec
  * Git
  * Clojure
  * C++
  * General

## Documentation

## Other Ways to Contribute

## Getting Help

  * IRC
  * Mailing Lists
  * Triages

## Asking Good Questions
