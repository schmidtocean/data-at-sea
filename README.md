# Data At Sea

A community-driven, GitHub Pages-hosted resource aggregate focused on deep ocean science data management across the expedition lifecycle. Built for easy community contribution via Discussion, Issues, and Pull Requests 

## Contributing

As a community resource, we accept
* Links to external resources, repositories, and tools
* Code snippets to add to our library of useful tools
* Documentation, changes, and suggestions for the wiki

To contribute, use the Quick Issue Links below or Make a Pull Request:

### Report an Issue

Help us improve Data At Sea by reporting bugs, requesting features, or suggesting improvements. Choose the type of issue you want to report:

---

#### 🐛 Bug Report
Found something that's not working? Report a bug with a tool or the website.

<a href="https://github.com/schmidtocean/data-at-sea/issues/new?labels=bug&template=bug_report.md&title=[BUG]%20" 
   class="btn btn-primary" 
   target="_blank">
  Report a Bug →
</a>

---

#### 📚 Documentation Issue
Help us improve the documentation - fix typos, clarify instructions, or suggest new content.

<a href="https://github.com/schmidtocean/data-at-sea/issues/new?labels=documentation&template=documentation.md&title=[DOCS]%20" 
   class="btn btn-primary" 
   target="_blank">
  Report Documentation Issue →
</a>

---

#### 🔬 Request a New Tool
Need a tool that doesn't exist yet? Want a tool modified to be more useful? Tell us what you need. The form will open with a structured template to help you describe your request.

<a href="https://github.com/schmidtocean/data-at-sea/issues/new?labels=new-tool&title=[TOOL%20REQUEST]%20&body=%23%23%20Tool%20Name%0A%0A%23%23%20Purpose%0AWhat%20should%20this%20tool%20do%3F%0A%0A%23%23%20Input%20Data%0AWhat%20data%20formats%20should%20it%20accept%3F%0A%0A%23%23%20Output%0AWhat%20should%20it%20produce%3F%0A%0A%23%23%20Use%20Case%0ADescribe%20a%20specific%20scenario%20where%20you%20would%20use%20this%20tool.%0A%0A%23%23%20Cruise%20Phase%0A-%20%5B%20%5D%20Pre-cruise%20planning%0A-%20%5B%20%5D%20At-sea%20operations%0A-%20%5B%20%5D%20Post-cruise%20processing%0A%0A%23%23%20Priority%0A-%20%5B%20%5D%20Critical%20-%20Blocking%20my%20work%0A-%20%5B%20%5D%20High%20-%20Very%20important%0A-%20%5B%20%5D%20Medium%20-%20Would%20be%20helpful%0A-%20%5B%20%5D%20Low%20-%20Nice%20to%20have%0A%0A%23%23%20Languages%20Preferred%0A-%20%5B%20%5D%20Python%0A-%20%5B%20%5D%20R%0A-%20%5B%20%5D%20MATLAB%2FOctave%0A-%20%5B%20%5D%20Any%20language%20is%20fine%0A%0A%23%23%20Additional%20Context%0AAdd%20any%20other%20information%2C%20examples%2C%20or%20references." 
   class="btn btn-primary" 
   target="_blank">
  Request a Tool →
</a>

---

### Issue Guidelines

#### For Bug Reports:
- Tool name and version
- Steps to reproduce the problem
- Expected vs actual behavior
- Error messages (if any)
- Your operating system and Python/R/MATLAB version

#### For Documentation Issues:
- Page URL or section name
- What's unclear or incorrect
- Suggested improvement

#### For Tool Requests:
The form opens with a template that asks you to describe:
- What the tool should do
- What data it works with
- When you'd use it (which cruise phase)
- How important it is to your work
- Your preferred programming language

---

### Make a Pull Request

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

## Architecture Diagram

Web content hosted on GitHub Pages is included in the root directory (_config.yml, Gemfile) while individual pages are hosted in the docs/ directory as markdown files. Each tool has a separate documentation page in docs/tool-docs/ to host notebooks in the browser. Each tool page includes direct download links to the respective tool. The tools are hosted in the tools/ directory under the root level to maintain separation of code for tools and code for documentation.

If you would like to add or change pages on the Data at Sea webpage, edit or add content in the docs/ folder. If you are a user adding new tools, add them in the tools/ directory, and create a corresponding documentation page in the docs/tool-docs/ directory.

```
┌──────────────────────────────────────┐     ┌──────────────────────────────────────┐
│     USER-FACING WEB CONTENT          │     │     INTERNAL REPO STRUCTURE          │
│ (schmidtocean.github.io/data-at-sea) │     │ (github.com/schmidtocean/data-at-sea)│
└──────────────────────────────────────┘     └──────────────────────────────────────┘

                                              /
* Home/Landing page                           ├ index.md
                                              │
                                              ├ docs/
* Pre-cruise                                  │ ├ pre-cruise.md
* At Sea                                      │ ├ at-sea.md
* Post-cruise                                 │ ├ post-cruise.md
* Data Repositories                           │ ├ repositories.md
* Discussion                                  │ ├ discussion.md
* Contributing                                │ ├ contributing.md
                                              │ └ tool-docs/
* Tools                                       │   ├ tool-overview.md
   + tool 1                                   │   ├ tool1.md
   + tool 2                                   │   └ tool2.md
                                              │
                                              ├ tools/
                                              │ ├ tool1/
                                              │ │ ├ tool1.ipynb
                                              │ │ └ requirements.txt
                                              │ └ tool2/
                                              │   ├ tool2.ipynb
                                              │   └ requirements.txt
                                              │
                                              ├ _config.yml
                                              ├ _templates
                                              ├ README.md
                                              ├ LICENSE
                                              └ Gemfile
```

