title=Contributing		
type=page
status=published
tags=community
tableOfContents=false
~~~~~~

Thanks for choosing to contribute to Apache Sling! The following are a set of guidelines to follow when contributing to this project.

## Code of Conduct

Being an Apache project, Apache Sling adheres to the Apache Software Foundation's
[Code of Conduct](https://www.apache.org/foundation/policies/conduct.html).

## Legal

Before contributing to the project, please make sure you understand the
[requirements and implications of contributing to the Apache Software Foundation](https://www.apache.org/foundation/how-it-works/legal.html).
An [Apache iCLA](https://www.apache.org/licenses/icla.pdf) is welcome if you start contributing regularly, and required if you later become
a committer.

## How to contribute

Apache Sling is a volunteer effort, so there is always plenty of work that needs to be accomplished. If you want to help supporting Apache
Sling, this page is intended as a starting point for specific contribution ideas. To further understand how the Sling community operates,
refer to the [Community Roles and Processes document](https://www.apache.org/foundation/how-it-works.html) and/or join our mailing lists.

See [Project Information](/project-information.html) for details about the tools mentioned below.

The Apache Sling project organizes its "to do" list using the Apache [JIRA issue tracking system](https://issues.apache.org/jira/browse/SLING).
No matter if you are a programmer or not, it is probably best to check JIRA first to figure out if the problem you identified is already
known. If not, please create a JIRA issue in which you try to describe to the best of your knowledge the bug that you want to fix or the
improvement that you would like to contribute. There are many recommendations on the Web on how to write a good bug report, like
[Haje Jan Kamps' How to write the perfect bug report](https://medium.com/@Haje/how-to-write-the-perfect-bug-report-6430f5a45cd) blog post.

If pull requests are familiar to you, the next step is to open one against one of our modules. More details about how the
project is structured in terms of repositories can be read on the
[Getting and Building Sling](/documentation/development/getting-and-building-sling.html) page.

For relatively large contributions (e.g. new modules), we recommend one of the following two approaches:

1. open a JIRA issue and send a pull request to the [Apache Sling Whiteboard project](https://github.com/apache/sling-whiteboard/)
2. open a JIRA issue and attach your source code to it as a zip or tar archive.

For people who are completely new to contributing to an Apache Software Foundation project, the
[Get Involved](https://www.apache.org/foundation/getinvolved.html) page provides you with enough resources to understand how the foundation
works and how its projects are structured - and don't hesitate to ask on our
[mailing lists](http://sling.apache.org/project-information.html#mailing-lists)!

### Testing

Each Sling module comes with an automated build, usually based on Apache Maven. Your change should be covered
by new unit tests that verify that the changes work as expected.

In case your changes are more far-reaching and the module you are contributing to is part of the
[Sling Starter](https://github.com/apache/sling-org-apache-sling-starter), it is a good idea to
also run the Sling Starter integration tests. This can be achieved by doing the following:

* Check out the [Sling Starter](https://github.com/apache/sling-org-apache-sling-starter) and 
  [Sling Starter Integration Tests](https://github.com/apache/sling-org-apache-sling-launchpad-testing)
  projects. This step can be skipped if you have followed the steps to checkout all Sling repositories
  as documented at [Getting and Building Sling](/documentation/development/getting-and-building-sling.html#getting-the-sling-source)
* Use the latest version of the bundle(s) you changed in the Sling Starter. Running `git grep ${ARTIFACT_ID}`
  will indicate the potential places where you need to make changes
* Run `mvn clean install` in the Sling Starter checkout. This runs a set of Smoke tests and allows the 
  integration tests to use the version of the starter that you just built
* Run `mvn clean install` in the Sling Starter Integration Tests checkout

Additionally, and PR you submit will eventually be built by Jenkins, with additional validations on top
of the plain Maven build.
