---
title: Discussion
nav_order: 9
---

# Community Discussion

Our forum is powered by GitHub Discussions.

<div style="text-align: center; margin: 40px 0;">
  <a href="https://github.com/schmidtocean/data-at-sea/discussions" 
     class="btn btn-primary btn-lg" 
     target="_blank">
    Visit Forum →
  </a>
</div>

## Quick Links

- [Ask a Question](https://github.com/schmidtocean/data-at-sea/discussions/new?category=q-a)
- [Suggest a New Tool](https://github.com/schmidtocean/data-at-sea/discussions/new?category=ideas)
- [View Announcements](https://github.com/schmidtocean/data-at-sea/discussions/categories/announcements)
- [Browse All Discussions](https://github.com/schmidtocean/data-at-sea/discussions)

# Community Discussion (alternate option)

<div id="discussions-list">Loading discussions...</div>

<a href="https://github.com/schmidtocean/data-at-sea/discussions/new" class="btn btn-primary">Start New Discussion</a>

<script>
fetch('https://api.github.com/repos/schmidtocean/data-at-sea/discussions')
  .then(r => r.json())
  .then(discussions => {
    const html = discussions.map(d => `
      <div style="padding: 15px; margin: 10px 0; border-left: 3px solid #3498db;">
        <h4 style="margin: 0;">
          <a href="${d.html_url}" target="_blank">${d.title}</a>
        </h4>
        <p style="margin: 5px 0; color: #666; font-size: 14px;">
          ${d.comments.totalCount} comments · ${d.category?.name}
        </p>
      </div>
    `).join('');
    document.getElementById('discussions-list').innerHTML = html;
  });
</script>
