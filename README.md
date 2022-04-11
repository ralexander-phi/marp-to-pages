<!--
theme: gaia
class:
 - invert
headingDivider: 2 
paginate: true
-->

<!--
_class:
 - lead
 - invert
-->

# Marp Action for GitHub

Presentations to Webpages: Instantly!

## What?

[Marp](https://marp.app/) lets you create slides from markdown (like this!).

This presentation is both a [website](https://alexsci.com/test-marp-action) and a [README.md](https://github.com/ralexander-phi/test-marp-action/blob/main/README.md).

## Why?

Treat your presentation the same way you treat code.

Use git to track changes. Pull requests to collaborate. Deploy to a webpage automatically.

See a bug? Open an issue or pull request!

## Setup

Want to create your own?

First, create a new repo [from the template repo](https://github.com/ralexander-phi/test-marp-action).

![](img/use-template.png)

## Configure GitHub Pages

[Setup publishing](https://help.github.com/en/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#choosing-a-publishing-source).

Remember the branch and URL you choose.

## Update Workflow

You'll update the workflow file over the next few slides. You can do this right in the GitHub web page (click on the pencil icon).

`.github/workflows/main.yml`

## `BASE_URL`

Set this to the domain you're using for GitHub Page.

If you add a custom domain later, you'll need to update this.

## `PUBLISH_TO_BRANCH`

Tell the build which branch you are using for GitHub Pages.

This is likely `gh-pages`. Set `PUBLISH_TO_BRANCH` to the correct branch.

## Update Workflow

Commit `.github/workflows/main.yml` back to `main` branch.

This will kick off the workflow.

## Check if the build succeeded

Click on Actions tab and see if the build succeeded.

![](img/click-actions.png)

You should now see the generated files in the `gh-pages` branch.

## Load your new web page

Any update to your site will take a few minutes to be visible. Be patient.

## Create your slides

Finally, start adding your own content.

You can [install and run marp-cli](https://github.com/marp-team/marp-cli/blob/master/README.md) locally to test out the content before publishing.

## Pull Request Previews

Push your slides to a new branch and create a pull request.

The workflow is triggered by the Pull Request and will build a preview page.

Click the link to see a preview of the built content.


## Running locally

Locally you'll run commands like:

```
npx @marp-team/marp-cli@latest README.md -o build/README.pdf
```

## As a workflow step

The workflow step equivalent is:

```
- name: Marp Build (README.pdf)
  uses: docker://marpteam/marp-cli:v1.7.0
  with:
    args: README.md -o build/README.pdf
  env:
    MARP_USER: root:root
```

Note the `args` match the previous slide.

## Customizing the build

Anything in the `build/` folder will be deployed.

You can perform other types of processing steps here as well.

## Learn more about Marp

This is a good time to learn more about Marp. Here's some resources:

- [CommonMark](https://commonmark.org/)
- [Cheat Sheet](https://commonmark.org/help/)
- [Themes](https://github.com/marp-team/marp-core/tree/master/themes)
- [CSS Themes](https://marpit.marp.app/theme-css)
- [Directives](https://marpit.marp.app/directives)
- [VS Code plugin](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)

## Example Sites

Known sites using this action are:

- [University of Illinois at Urbana-Champaign's CS 199 Even More Practice](https://cs199emp.netlify.app/) [(code)](https://github.com/harsh183/emp-125)
- [Exploring agent based models](https://roiarthurb.github.io/Talk-UMMISCO_06-07-2020/) [(code)](https://github.com/RoiArthurB/Talk-UMMISCO_06-07-2020)

Send a [pull request](https://github.com/ralexander-phi/test-marp-action) to get your site added.

## Publish your slides

When you are ready to share your presentation, commit or merge to `main` and your content on GitHub Pages will automatically update.

# 🎉
<!--
_class:
 - lead
 - invert
-->
### Hooray!


