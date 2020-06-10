# Package Doc URL Testing Monorepo

Probing the intersection of monorepo packages, Markdown, Github and doc URLs.

## Huh?

When Markdown files are added to a monorepo, the links need to make sense on the local fs, to Github and when the packages are published to NPM.
Getting this all working at the same time isn't trivial.

This repo sets up a super-simple package with links using different URL formulations.
Look at [the code](/raw/HEAD/packages/not-a-real-package/README.md),
then see what the package looks like when it's [published on NPM](https://www.npmjs.com/package/@molomby/not-a-real-package).

## TL;DR

**Configure your `package.json` [correctly](https://docs.npmjs.com/files/package.json.html#repository)**

* Your `repository.url` should point to the _root_ of your repo
* Use the `repository.directory` prop to specify the path to the package

Eg..

```json
"repository": {
  "type" : "git",
  "url" : "https://github.com/molomby/package-doc-url-testing.git",
  "directory": "packages/not-a-real-package"
}
```

**When linking to other docs, use URLs relative to the repo root**

Ie. starting with a slash: `/`.
These work reliably on GitHub and NPM.

## Related Info

* The [`@molomby/not-a-real-package` package on NPM](https://www.npmjs.com/package/@molomby/not-a-real-package)
* How we handle [doc links in the Keystone Monorepo](https://github.com/keystonejs/keystone/issues/2041#issuecomment-566802733)
* Also the [Keystone Style Guile on Links](https://github.com/keystonejs/keystone/blob/master/STYLE_GUIDE.md#links)
* NPM [`package.json` repo section docs](https://docs.npmjs.com/files/package.json.html#repository)

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
