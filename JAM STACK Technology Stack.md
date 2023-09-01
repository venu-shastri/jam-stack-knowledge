## JAM STACK Technology Stack

- JavaScript Based Static Site Generator
  - Next.js and Gatsby
  - Templating Language
- CMS
  - Traditional CMS
  - Head Less CMS
    - Api based
    - Git Based
      - Netlify CMS
- APIs
- Deployment Platform

### Gatsby

---

- Gatsby (https://gatsbyjs.org) is a static site generator for React
- Pages are created using React components, then are run through a build process which produces static
  HTML files and associated assets.

```
//Install Gatsby Command Line Interface
npm install -g gatsby-cli

//Check Installation and Version 
gatsby --version 
```

## Netlify CMS

- Netlify CMS is a free, open source headless CMS created by Netlify
- The content is stored as images and Markdown files in a Git repository
- Netlify CMS provides a React single-page application with a rich text editor so that content creators don’t have to write Markdown directly
- Netlify CMS can be used with any platform, such as Hugo, Jekyll, Nuxt, as well as Gatsby.
- Netlify CMS supports several different backends for storing its data
  - GitHub , Git Lab, Bitbucket , Git Gateway backend

### How Netlify CMS Works

---

> Netlify CMS is configured with a YAML file named **config.yml.** This file configures the
> different resources managed by the CMS. These resources are divided up into **collections**.
> Each collection will have its own **section** in the CMS user interface, and each collection
> defines a set of **fields**. These **fields** determine **which UI control**s will appear when editing
> content in each collection.



```yaml
collections:
 - name: "blog"
 - folder: "src/pages/blog"
 - fields:
	- label: "Title"
	  name: "title"
      widget: "string"
    - label: "Publish Date"
      name: "date"
      widget: "datetime"
    - label: "Body"
      name: "body"
      widget: "markdown"
```



#### Setting up Netlify CMS - Gatsby

---



```
//The Netlify CMS application
npm install netlify-cms-app

//The Netlify CMS Gatsby plugin
npm install gatsby-plugin-netlify-cms

```

