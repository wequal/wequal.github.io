---
layout: default
title: CallRecorder Privacy Policy
description: Privacy policy for the CallRecorder app
---

{% assign app = site.data.apps | where: "slug", "callrecorder" | first %}
{% include privacy-policy.html app=app %}
