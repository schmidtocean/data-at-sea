---
title: Contributing
layout: default
nav_order: 7
---

# Contributing

As a community resource, we accept
* Links to external resources, repositories, and tools
* Code snippets to add to our library of useful tools
* Documentation, changes, and suggestions for the wiki

To contribute, use the Quick Issue Links below or Make a Pull Request:

## Report an Issue

Help us improve Data At Sea by reporting bugs, requesting features, or suggesting improvements.

## Quick Issue Links

Choose the type of issue you want to report:

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 30px 0;">
  
<div style="border: 2px solid #d73a49; padding: 20px; border-radius: 8px;">
  <h3 style="color: #d73a49; margin-top: 0;">🐛 Bug Report</h3>
  <p>Report a problem with a tool or the website</p>
  <a href="https://github.com/schmidtocean/data-at-sea/issues/new?labels=bug&template=bug_report.md&title=[BUG]%20" 
     class="btn btn-outline" 
     target="_blank">
    Report Bug →
  </a>
</div>

<div style="border: 2px solid #0366d6; padding: 20px; border-radius: 8px;">
  <h3 style="color: #0366d6; margin-top: 0;">💡 Feature Request</h3>
  <p>Suggest a new tool or feature</p>
  <a href="https://github.com/schmidtocean/data-at-sea/issues/new?labels=enhancement&template=feature_request.md&title=[FEATURE]%20" 
     class="btn btn-outline" 
     target="_blank">
    Request Feature →
  </a>
</div>

<div style="border: 2px solid #28a745; padding: 20px; border-radius: 8px;">
  <h3 style="color: #28a745; margin-top: 0;">📚 Documentation</h3>
  <p>Improve or clarify documentation</p>
  <a href="https://github.com/schmidtocean/data-at-sea/issues/new?labels=documentation&template=documentation.md&title=[DOCS]%20" 
     class="btn btn-outline" 
     target="_blank">
    Suggest Docs Change →
  </a>
</div>

<div style="border: 2px solid #6f42c1; padding: 20px; border-radius: 8px;">
  <h3 style="color: #6f42c1; margin-top: 0;">🔬 Tool Request</h3>
  <p>Request a new analysis tool</p>
  <a href="https://github.com/schmidtocean/data-at-sea/issues/new?labels=new-tool&title=[TOOL REQUEST]%20&body=%23%23%20Tool%20Name%0A%0A%23%23%20Purpose%0AWhat%20should%20this%20tool%20do%3F%0A%0A%23%23%20Input%20Data%0AWhat%20data%20formats%20should%20it%20accept%3F%0A%0A%23%23%20Output%0AWhat%20should%20it%20produce%3F%0A%0A%23%23%20Phase%0A-%20%5B%20%5D%20Pre-cruise%0A-%20%5B%20%5D%20At-sea%0A-%20%5B%20%5D%20Post-cruise%0A%0A%23%23%20Priority%0A-%20%5B%20%5D%20Critical%0A-%20%5B%20%5D%20Important%0A-%20%5B%20%5D%20Nice%20to%20have" 
     class="btn btn-outline" 
     target="_blank">
    Request Tool →
  </a>
</div>

</div>

## Making a Pull Request

1. **Fork the repository**: Click the "Fork" button at the top right of this repository to create your own copy.

2. **Clone your fork**: Clone your forked repository to your local machine using git command line tools or GitHub Desktop:
   ```bash
   git clone https://github.com/YOUR-USERNAME/data-at-sea-wiki.git
   cd data-at-sea-wiki
   ```

3. **Create a branch**: Create a new branch for your changes:
   ```bash
   git checkout -b your-feature-branch
   ```

4. **Make your changes**: Edit or add content to the wiki. Ensure your changes are clear, accurate, and well-documented. Software tools, notebooks, and snippets should be added to the tools/ directory. Additional documentation or new pages can be added in the docs/ directory.

5. **Commit your changes**: Commit your changes with a descriptive message:
   ```bash
   git add .
   git commit -m "Add description of your changes"
   ```

6. **Push to your fork**: Push your changes to your forked repository:
   ```bash
   git push origin your-feature-branch
   ```

7. **Open a Pull Request**: Go to the original repository on GitHub and click "New Pull Request". Select your fork and branch, then provide a clear description of your changes.

8. **Review process**: Wait for maintainers to review your pull request. Be prepared to make revisions based on feedback.
