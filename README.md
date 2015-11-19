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

1. *Figure out what you want to work on.* There is endless work to be done against puppet core and modules. If you have
a problem or feature that you think you want to work on, the first step is to make sure there's a ticket for that work.
Go to [tickets.puppetlabs.com](https://tickets.puppetlabs.com/) and do a quick search to see if a ticket describing the
work you want to do already exists. All core projects will have their own Jira project (e.g. PUP for puppet, FACT for facter)
and there is a MODULES project for modules work. If there is a ticket, great! Reference that one. If not please create one.
Browsing tickets is another great way to find an idea if you don't already have something in mind.

2. *Sign the CLA* (if you're working on core projects). If you want to contribute to puppet core, you'll have to sign
the [Contributor's License Agreement](https://cla.puppetlabs.com). This basically just says "hey it's okay if you want
to use my code in your project". This is not needed for contributing to modules.

3. *Clone and fork the repository*. Once you know what you want to work on, it's time to grab some code. All the projects
live on GitHub under the [puppetlabs](https://github.com/puppetlabs) GitHub organization. Find the repo for the project
you're working on, for example [puppetlabs/puppet](https://github.com/puppetlabs/puppet) or
[puppetlabs/puppetlabs-apache](https://github.com/puppetlabs/puppetlabs-apache). Then create a fork of the repository
and clone it locally so you can get started. If you need more help on git and git work flows, check out the Resources
section.

4. *Create a topic branch.* We prefer to merge pull requests from topic branch to master rather than master to master.
Please create a git topic branch where you can do your work.

5. *Make your changes.* Make the fix or add the feature you want to add. Please make sure to follow the
(contributing guidelines)[https://github.com/puppetlabs/puppet/blob/master/CONTRIBUTING.md] and commit as you go using
correctly formatted commit messages. You can find resources for help learning the programming language you need to use
and should absolutely ask for help on IRC if you're feeling stuck. Our community is full of helpful friendly people
who would love to answer your questions.

6. *Run and write tests* as appropriate. Most of our project will have a built in tests suit to catch regressions. As
you make your changes, please run spec tests to make sure something hasn't been accidentally broken. Most of our
repositories will run tests automatically when a pull request is submitted. If tests are failing we will likely kick
the pull request back to you, so to speed up the process please run tests on your own.  In many situations
you will also need to update tests or even write new ones. Tests can often be even trickier than fixing the code,
so again please reach out if you're stuck.

7. *Open a pull request.* Once your work and your tests are ready to go it's time to open a pull request! Please
take a second to double check that your work follows the contributing guidelines and then open a pull request
targeting the master branch. Always target master unless it's a special case and you've spoken with someone
who has told you which branch to target.

8. *Be ready for feedback and discussion.* Once your pull request is in you're not really done, you've just entered the
next phase in the process. Many people think that once they open a pull request they're done, but in almost all cases
we'll have feedback, questions, or changes we'd like you to make. Please keep an eye on the pull request or your GitHub
notifications so you're ready to respond to feedback. That way we can get your code reviewed and merged must faster.


### Process

### Getting Help/Resources

### Tips and Tricks

## Documentation
