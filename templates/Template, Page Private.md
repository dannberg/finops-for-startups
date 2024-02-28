---
title: Page Title
draft: true
tags:
  - finops
---
# [[<% tp.date.now("YYYY-MM-DD") + " " + tp.file.title %>]]
<% await tp.file.move("/private/" + tp.date.now("YYYY-MM-DD") + " " + tp.file.title) %>
