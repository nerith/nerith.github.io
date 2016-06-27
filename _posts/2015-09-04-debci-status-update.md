---
layout: post
title: debci now supports status alerts
---

After some work, debci now supports showing a status alert view in its
web UI. The view allows debci admins to get an overview of the alerts
reported by debci.

Currently, the view only shows packages that have reported tmpfail
statuses although it should encompass more in the future.

Below is a screenshot of the status alert view running on
[autopkgtest.ubuntu.com](http://autopkgtest.ubuntu.com).

![debci status alert view](/assets/debci/debci-alert.png)

The following commits were responsible for this feature:

[Commit 2a3e61f2](http://anonscm.debian.org/cgit/collab-maint/debci.git/commit/?id=2a3e61f2311447015fc9ac710eaacd8293eb7871)

[Commit 2bd67abf](http://anonscm.debian.org/cgit/collab-maint/debci.git/commit/?id=2bd67abf3e58d9016bfb3a06aa866127044503a1)

[Commit 90302f20](http://anonscm.debian.org/cgit/collab-maint/debci.git/commit/?id=90302f201d8ee0e16367216abd4fc2a45e4dc3b2)
