---
layout: default
---

<div id="readme-content"></div>

<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
<script>
  fetch('README.md')
    .then(r => r.text())
    .then(text => {
      document.getElementById('readme-content').innerHTML =
        marked.parse(text, { gfm: true, breaks: true });
    });
</script>
