---
layout: default
title: FileShare Support
description: Support and bug reports for the FileShare app
---

{% assign app = site.data.apps | where: "slug", "fileshare" | first %}
{% include support.html app=app %}
