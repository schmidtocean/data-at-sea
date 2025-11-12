# Data At Sea Wiki

A community-driven, GitHub Pages-hosted resource aggregate focused on deep ocean science data management across the expedition lifecycle. Built for easy community contribution via Discussion, Issues, and Pull Requests 

## Contributing

As a community resource, we accept
* Links to external resources, repositories, and tools
* Code snippets to add to our library of useful tools
* Documentation, changes, and suggestions for the wiki

To contribute, please follow these steps:

### Making a Pull Request

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

4. **Make your changes**: Edit or add content to the wiki. Ensure your changes are clear, accurate, and well-documented.

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

### Help I Don't Understand Pull Requests!

We get it, not everyone is familiar with Git and you probably have incredible skills in other areas that we want to share with the community. If you are not confident in creating a pull request yourself, [open a discussion](https://github.com/schmidtocean/data-at-sea/discussions) with your content and the maintainers will work with you to get it into the community resource.

### Something is Broken

As a community hub, we depend on external tools, links, and libraries, which can change without us knowing. If something breaks we're happy to investigate and update as needed. [Open an issue](https://github.com/schmidtocean/data-at-sea/issues) if something isn't working as expected.

## Architecture Diagram

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
                                              │ └ tools/
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
                                              ├ README.md
                                              ├ LICENSE
                                              └ Gemfile
```

Web content hosted on GitHub Pages is included in the root directory (_config.yml, Gemfile) while individual pages are hosted in the docs/ directory as markdown files. Each tool has a separate documentation page in docs/tools/ to host notebooks in the browser. Each tool page includes direct download links to the respective tool. The tools are hosted in the tools/ directory under the root level to maintain separate of code for tools and code for documentation.
