---
aliases: []
tags: []
---

---
tags:
  - 📚Book
title: "{{title}}"
subtitle: "{{subtitle}}"
author: [{{author}}]
category: [{{category}}]
publisher: {{publisher}}
publish: {{publishDate}}
total: {{totalPage}}
isbn10: {{isbn10}} 
isbn13: {{isbn13}}
cover: {{coverUrl}}
localCover: {{localCoverImage}}
status: unread
created: {{DATE:YYYY-MM-DD HH:mm:ss}}
updated: {{DATE:YYYY-MM-DD HH:mm:ss}}
---

<%* if (tp.frontmatter.localCover && tp.frontmatter.localCover.trim() !== "") { tR += `![[${tp.frontmatter.localCover}|150]]` } %>

# {{title}}
{{description}}