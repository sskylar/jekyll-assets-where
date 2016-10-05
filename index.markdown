---
---

# Using `where` with single word titles:

{% assign doc = site.docs | where:'title','Titlewithoutspaces' | first %}

- {{ doc.title | default: 'null' }}

# Using `where` with multiple word titles:

{% assign doc = site.docs | where:'title','Title with spaces' | first %}

- {{ doc.title | default: 'null' }}
