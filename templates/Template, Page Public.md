---
title: Page Title
draft: true
tags:
  - finops
---
<% await tp.file.move("/content/" + tp.date.now("YYYY-MM-DD") + " " + tp.file.title) %>
