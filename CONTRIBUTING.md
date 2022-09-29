# Eclipse OpenJ9 Development

The Eclipse OpenJ9&trade; website is built with [Gatsby.js](https://www.gatsbyjs.org/). See the Gatsby [quick start guide](https://www.gatsbyjs.org/docs/quick-start) for the basics.

## Prerequisites

- **Node 10+**
  Download Node.js from https://nodejs.org/en/

- [**Gatsby.js**](https://www.gatsbyjs.org)
  When Node is installed, run the following command to install Gatsby.js:

  ```bash
    npm install -g gatsby-cli
  ```

- **Install Node dependencies** Clone the website Git repo and install the dependencies with the following commands:

  ```bash
    git clone https://github.com/eclipse-openj9/openj9-website.git
    cd website

    npm install
  ```

## Developing locally

1. Run the development server:

```bash
gatsby develop
```

This command compiles your changes as you develop and hosts the website at http://localhost:8000. To explore GraphQL queries that Gatsby exposes, use http://localhost:8000/__graphql.

:pencil: **Note about clearing your Cache:**
Sometimes when developing locally, the website shows cached content from previous versions of the website. To clear the cache before developing, run the following command:

```bash
gatsby clean
```

## Update Latest release section
Open `news-page-content/latestRelease.md` and edit it as required and this will automatically be converted to HTML during the build.

## Redirecting page

If you change the page URL, you must add a redirect to prevent broken links, especially from external sources.

1. Open the `gatsby-node.js` file found at the root of the project
2. In the redirects section, add the following code snippet:

```
createRedirect({
    fromPath: `/old/path`,
    toPath: `/new/path`,
    isPermanent: true
  });
```

Note, you need to provide only the path.





