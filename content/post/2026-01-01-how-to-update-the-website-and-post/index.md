---
date: '2026-01-01T21:49:57-07:00'
title: How to update this website and post
---

1.  Make a file in the content/post directory. The file name should be in the format YYYY-MM-DD-title/index.md, where YYYY-MM-DD is the date of the post, and title is a short descriptive title for the post.
2.  In the console, run `blogdown::serve_site()` from the console or equivalently, click on the RStudio addin "Serve Site" 
3.  When in doubt, run `blogdown::check_site()`
4.  run blogdown::build_site() to built the webpages
5.  commit to GitHub and push to origin
6.  The updated website will be ready for viewing at: <https://fongching.netlify.app/>
