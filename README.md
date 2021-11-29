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

[Marp Action](https://github.com/ralexander-phi/marp-action) lets you automatically deploy your presentation to [GitHub Pages](https://pages.github.com/).

This presentation is both a [website](https://alexsci.com/test-marp-action) and a [README.md](https://github.com/ralexander-phi/test-marp-action/blob/dev/README.md).

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

Remember the branch and URL shown.

## Update Workflow

You'll update the workflow files over the next few slides. You can do this right in the GitHub web page (click on the pencil icon).

## `.github/workflows/main.yml`

The `main.yml` workflow publishes your slides to GH Pages. Consider changing the following settings:

- `BASE_URL`
  Set this to the domain you're using for GitHub Page (from earlier).
  If you add a custom domain later, you'll need to update this.
- `PUBLISH_TO_BRANCH`
  Tell the build which branch you are using for GitHub Pages (you picked this earlier).
  This is likely either `main` or `gh-pages`. Set `PUBLISH_TO_BRANCH` to the correct branch.

## `.github/workflows/build-preview.yml`

The `build-preview.yml` workflow builds preview slides for all pull requests submitted for the `dev` branch. You do not need to change anything in this workflow.

## Update Workflow

Commit `.github/workflows/main.yml` back to `dev` branch.

This will kick off a build.

## Check if the build succeeded

Click on Actions tab and see if the build succeeded.

![](img/click-actions.png)

## Load your new web page

Any update to your site will take a few minutes to be visible. Be patient.

## Create your slides

Finally, start adding your own content.

You can [install and run marp-cli](https://github.com/marp-team/marp-cli/blob/master/README.md) locally to test out the content before publishing.

Each pull request opened for the `dev` branch will contain an artifact with preview slides in HTML and PDF. For information on how download the artifact, see [Downloading workflow artifacts](https://docs.github.com/en/actions/managing-workflow-runs/downloading-workflow-artifacts) in _GitHub Actions Documentation_.

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

When you are ready to share your presentation, commit or merge to `dev` and your content on GitHub Pages will automatically update.

# 🎉
<!--
_class:
 - lead
 - invert
-->
### Hooray!
