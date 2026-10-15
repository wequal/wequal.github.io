---
layout: default
title: WePaint Privacy Policy
description: Privacy policy for the WePaint app
---

{% assign app = site.data.apps | where: "slug", "wepaint" | first %}
{% include privacy-policy.html app=app %}
