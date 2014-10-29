# Contributing to Knife-Lpar

We are glad you want to contribute to Knife-Lpar!

We utilize **Github Issues** for issue tracking and contributions. You can contribute in two ways:

1. Reporting an issue or making a feature request [here](#issues).
2. Adding features or fixing bugs yourself and contributing your code to Chef.

## Contribution Process

We have a 3 step process that utilizes **Github Issues**:

1. Sign our
  [Individual Contributor License Agreement (CLA)](http://supermarket.getchef.com/icla-signatures)
  or [Corporate CLA](http://supermarket.getchef.com/ccla-signatures) online once.
2. Create a Github Pull Request.
3. Do [Code Review](#cr) with the **Chef Engineering Team** on the pull request.

### <a name="pulls"></a> Chef Pull Requests

Chef is built to last. We strive to ensure high quality throughout the Chef experience. In order to ensure
  this, we require a couple of things for all pull requests to Chef:

1. **Tests:** To ensure high quality code and protect against future regressions, we require all the
  code in Chef to have at least unit test coverage. See the [spec/unit](https://github.com/opscode/knife-container/tree/master/spec/unit)
  directory for the existing tests and use ```bundle exec rake spec``` to run them.
2. **Green Travis Run:** We use [Travis CI](https://travis-ci.org/) in order to run our tests
  continuously on all the pull requests. We require the Travis runs to succeed on every pull
  request before being merged.

In addition to this it would be nice to include the description of the problem you are solving
  with your change. You can use [Chef Issue Template](#issuetemplate) in the description section
  of the pull request.

### <a name="cr"></a> Chef Code Review Process

The Chef Code Review process happens on Github pull requests. See
  [this article](https://help.github.com/articles/using-pull-requests) if you're not
  familiar with Github Pull Requests.

Once you a pull request, the **Chef Engineering Team** will review your code
  and respond to you with any feedback they might have. The process at this point is as follows:

1. 2 thumbs-ups are required from the **Chef Engineering Team** for all merges.
2. When ready, your pull request will be tagged with label `Ready For Merge`.
3. Your patch will be merged into `master` including necessary documentation updates
  and you will be included in `CHANGELOG.md`. Our goal is to have patches merged in 2 weeks
  after they are marked to be merged.

If you would like to learn about when your code will be available in a release of Chef, read more about
  [Chef Release Process](#release).

### Contributor License Agreement (CLA)
Licensing is very important to open source projects. It helps ensure the
  software continues to be available under the terms that the author desired.

Chef uses [the Apache 2.0 license](https://github.com/opscode/chef/blob/master/LICENSE)
  to strike a balance between open contribution and allowing you to use the
  software however you would like to.

The license tells you what rights you have that are provided by the copyright holder.
  It is important that the contributor fully understands what rights they are
  licensing and agrees to them. Sometimes the copyright holder isn't the contributor,
  most often when the contributor is doing work for a company.

To make a good faith effort to ensure these criteria are met, Chef requires an Individual CLA
  or a Corporate CLA for contributions. This agreement helps ensure you are aware of the
  terms of the license you are contributing your copyrighted works under, which helps to
  prevent the inclusion of works in the projects that the contributor does not hold the rights
  to share.

It only takes a few minutes to complete a CLA, and you retain the copyright to your contribution.

You can complete our
  [Individual CLA](https://secure.echosign.com/public/hostedForm?formid=PJIF5694K6L) online.
  If you're contributing on behalf of your employer and they retain the copyright for your works,
  have your employer fill out our
  [Corporate CLA](https://secure.echosign.com/public/hostedForm?formid=PIE6C7AX856) instead.

### Chef Obvious Fix Policy

Small contributions such as fixing spelling errors, where the content is small enough
  to not be considered intellectual property, can be submitted by a contributor as a patch,
  without a CLA.

As a rule of thumb, changes are obvious fixes if they do not introduce any new functionality
  or creative thinking. As long as the change does not affect functionality, some likely
  examples include the following:

* Spelling / grammar fixes
* Typo correction, white space and formatting changes
* Comment clean up
* Bug fixes that change default return values or error codes stored in constants
* Adding logging messages or debugging output
* Changes to ‘metadata’ files like Gemfile, .gitignore, build scripts, etc.
* Moving source files from one directory or package to another

**Whenever you invoke the “obvious fix” rule, please say so in your commit message:**

```
------------------------------------------------------------------------
commit 370adb3f82d55d912b0cf9c1d1e99b132a8ed3b5
Author: danielsdeleo <dan@opscode.com>
Date:   Wed Sep 18 11:44:40 2013 -0700

  Fix typo in config file docs.

  Obvious fix.

------------------------------------------------------------------------
```

## <a name="issues"></a> Chef Issue Tracking

Chef Issue Tracking is handled using Github Issues.

If you are familiar with Chef and know the component that is causing you a problem or if you
  have a feature request on a specific component you can file an issue in the corresponding
  Github project. All of our Open Source Software can be found in our
  [Github organization](https://github.com/opscode/).

In order to decrease the back and forth an issues and help us get to the bottom of them quickly
  we use below issue template. You can copy paste this code into the issue you are opening and
  edit it accordingly.

<a name="issuetemplate"></a>
```
### Version:
[Version of the project installed]

### Environment: [Details about the environment such as the Operating System, cookbook details, etc...]

### Scenario:
[What you are trying to achieve and you can't?]



### Steps to Reproduce:
[If you are filing an issue what are the things we need to do in order to repro your problem?]


### Expected Result:
[What are you expecting to happen as the consequence of above reproduction steps?]


### Actual Result:
[What actually happens after the reproduction steps?]
```