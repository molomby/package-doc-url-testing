# Package Doc URL Testing Monorepo

Probing the intersection of monorepo packages, Markdown, Github and doc URLs.

## TL;DR

**Configure your `package.json` [correctly](https://docs.npmjs.com/files/package.json.html#repository)**

* Your `repository.url` should point to the _root_ of your repo
* Use the `repository.directory` prop to specify the path to the package

Eg..

```js
  "repository": {
    "type" : "git",
    "url" : "https://github.com/molomby/package-doc-url-testing.git",
    "directory": "packages/not-a-real-package"
  }
```

**When linking to other docs, use URLs relative to the repo root**

Ie. starting with a slash: `/`.
These work reliably on GitHub and NPM.

## Test Links

You're currently reading the Repo README, available at:

* [Relative to this file](README.md)
* [Relative to the repo root](/README.md)

We have a package you should check out at either:

* [Relative to this file](packages/not-a-real-package/README.md)
* [Relative to the repo root](/packages/not-a-real-package/README.md)

See also the the other doc at:

* [Relative to this file](OTHER_DOC.md)
* [Relative to the repo root](/OTHER_DOC.md)
