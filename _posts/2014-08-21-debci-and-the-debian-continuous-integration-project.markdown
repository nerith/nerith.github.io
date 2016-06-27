---
layout: post
title:  "debci and the Debian Continuous Integration Project"
date:   2014-08-21 16:21:27
categories: gsoc
---

![]({{site.baseurl}}/assets/gsoc/gsoc14.png)

Over the summer, I worked on the [Debian Continuous Integration project](http://ci.debian.net)
under my mentor Antonio Terceiro as part of the Google Summer of Code.

My project involved improving the web interface of debci. I had to implement
support for multiple suites and architectures, reduce the dependency the UI
had on Javascript, and provide more information to package maintainers.

Before diving into more detail, I would like to thank my mentor and
[Martin Pitt](http://www.piware.de) for giving me feedback on my interface
work during the summer.

# debci

debci runs tests against packages in Debian using the DEP-8 specification and
uses autopkgtest to run the tests on backends (currently schroot and LXC). The
project has the potential to increase the rate at which Debian is released.

# The debci web UI

Before GSoC started, the web UI relied entirely upon Javascript for displaying
information in the web UI. To fix this, the web interface was rewritten using
Ruby and ERB templates. Due to this, the interface now has alternatives
to the Javascript functionality (such as the browse by prefix for the package
search and status information for the data charts). Also, the package page and
the package history page are no longer reliant on Javascript.

In addition, the UI was updated for upcoming support for multiple suites and
architectures. The interface that was present before GSoC only supported
unstable/amd64. After three months of work, the UI supports displaying multiple
suites and architectures in the web UI.

# Walkthrough
The homepage of the web interface displays a news feed, browse by prefix links,
and package search (JS).

![debci's main page]({{ site.url }}/assets/gsoc/debci_main.png)

After choosing a browse by prefix link, the interface displays packages under
that prefix along with their current overall status on all architectures
('Passing everywhere' or the architecture(s) the package is failing).

![debci's package listing]({{ site.url }}/assets/gsoc/debci_listing.png)

When a package is chosen from the list, the interface displays that package's
page which shows the testing status for the package on each suite/architecture.
If a status is chosen, the test history on the suite/architecture
for the package is shown.

![debci's test history]({{ site.url }}/assets/gsoc/debci_history.png)

The status page displays the data charts (Pass/fail and Pass percentage)
for all available suite/architectures.


![debci status charts]({{site.url}}/assets/gsoc/status.png)

# What this project means for Debian
As mentioned above, the Debian Continuous Integration project has the potential
to increase the rate at which Debian is released. The project also has the
potential to improve Debian package quality and the stability of the Debian
system.

# The future
Although Google Summer of Code is over, I am going to continue working on
debci's web UI and start working on other debci features.
