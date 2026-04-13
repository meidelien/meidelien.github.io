---
title: "AdiFind"
excerpt: "AdiFind workflow overview with processing steps, QuPath validation views, and example downloads."
collection: portfolio
permalink: /adifind/
redirect_from:
  - /portfolio/adifind/
author_profile: false
---

<div class="adifind-page__intro">
  <img
    class="adifind-page__logo"
    src="{{ '/images/adifind_logo_cropped.png' | relative_url }}"
    alt="AdiFind logo">

  AdiFind is a digital pathology workflow for inspecting adipocyte-related regions in whole-slide images.
  The figures below show how the example slide moves from tissue detection to windowed processing and final annotated output,
  with additional GUI and QuPath views for validation.
</div>

<div class="adifind-page__actions">
  <a class="btn btn--info" href="{{ site.data.adifind.downloads.svs.path | relative_url }}">
    {{ site.data.adifind.downloads.svs.label }}
  </a>
  <a class="btn" href="{{ site.data.adifind.downloads.validation_zip.path | relative_url }}">
    {{ site.data.adifind.downloads.validation_zip.label }}
  </a>
</div>

{% include adifind_entries.html %}
