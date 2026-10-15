---
layout: default
title: FileShare Privacy Policy
description: Privacy policy for the FileShare app
---

{% assign app = site.data.apps | where: "slug", "fileshare" | first %}
{% include privacy-policy.html app=app %}
