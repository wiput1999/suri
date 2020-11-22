# Suri

Suri is your own link shortener that's easily deployed as a static site (for
free).

Suri doesn't give a 💩 about "technically superior" `3xx` server redirects. Suri
doesn't want a server (or "serverless" 🙄), or even a database for that matter.
Suri just wants a static site to get the job done – easy to deploy, and free to
host in a number of places.

This project was modified from
[https://github.com/jstayton/suri](https://github.com/jstayton/suri)

## Getting Started

### Manage Links

Links are managed through [`src/links.json`](src/links.json), which is seeded
with a few examples to start:

```json
{
  "/": "https://github.com/jstayton/suri",
  "1": "https://fee.org/articles/the-use-of-knowledge-in-society/",
  "gh": "https://github.com/jstayton"
}
```

It couldn't be simpler: the key is the "shortlink" path that gets redirected,
and the value is the target URL. Keys can be as short or as long as you want,
using whatever mixture of characters you want. `/` is a special entry for
redirecting the root path.

Go ahead and make an edit, then commit and push to your repository. The hosting
provider you chose above should automatically build and deploy your change.
That's it!

_Pro tip_: Bookmark the page to
[edit `src/links.json` directly in GitHub](https://github.com/jstayton/suri/edit/master/src/links.json)
(or wherever), and use the default commit message that's populated. Now show me
a link shortener that's easier than that!

### Install Manually

To install Suri somewhere else, or just on your own machine:

1. Fork this repository to create your own copy and clone to your machine.

1. Make sure you have a compatible version of [Node.js](https://nodejs.org/)
   (see `engines.node` in [`package.json`](package.json)).
   [nvm](https://github.com/nvm-sh/nvm) is the recommended installation method
   on your own machine:

   ```bash
   $ nvm install
   ```

1. Install dependencies with npm:

   ```bash
   $ npm install
   ```

1. Build the static site:

   ```bash
   $ npm run build
   ```

1. Deploy the generated `_site` directory to its final destination.
