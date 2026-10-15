---
layout: default
title: WePaint Support
description: Support and bug reports for the WePaint app
---

{% assign app = site.data.apps | where: "slug", "wepaint" | first %}
{% include support.html app=app %}
