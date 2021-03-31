# saebursa.netlify.app

personal update list product in my shop

## Sponsor

* [Anonim](t.me/imam_sf)
* [Intagram](https://instagram.com/pmm_umm91)
* [Youtube](https://youtube.com/channel/UCShlGVaP3Y4BUAxE56OChdg)

## Status build

[![Netlify Status](https://api.netlify.com/api/v1/badges/042e2bcc-2830-4c76-a005-e9fae9a1f729/deploy-status)](https://app.netlify.com/sites/saebursa/deploys)

## Demos

* [Netlify](https://saebursa.netlify.app/)

## Deploy this to your own site

These builders are amazing—try them out to get your own Eleventy site in a few clicks!

* [Get your own Eleventy web site on Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/xienli/saebursa.git)

## Getting Started

### 1. Clone this Repository

```
git clone https://github.com/xienli/saebursa.git blog-name
```


### 2. Navigate to the directory

```
cd blog-name
```

Specifically have a look at `.eleventy.js` to see if you want to configure any Eleventy options differently.

### 3. Install dependencies

```
npm install
```

### 4. Edit _data/metadata.json

### 5. Run Eleventy

```
npx eleventy
```

Or build and host locally for local development
```
npx eleventy --serve
```

Or build automatically when a template changes:
```
npx eleventy --watch
```

Or in debug mode:
```
DEBUG=* npx eleventy
```

### Implementation Notes

* `about/index.md` shows how to add a content page.
* `posts/` has the blog posts but really they can live in any directory. They need only the `post` tag to be added to this collection.
* Add the `nav` tag to add a template to the top level site navigation. For example, this is in use on `index.njk` and `about/index.md`.
* Content can be any template format (blog posts needn’t be markdown, for example). Configure your supported templates in `.eleventy.js` -> `templateFormats`.
	* Because `css` and `png` are listed in `templateFormats` but are not supported template types, any files with these extensions will be copied without modification to the output (while keeping the same directory structure).
* The blog post feed template is in `feed/feed.njk`. This is also a good example of using a global data files in that it uses `_data/metadata.json`.
* This example uses three layouts:
  * `_includes/layouts/base.njk`: the top level HTML structure
  * `_includes/layouts/home.njk`: the home page template (wrapped into `base.njk`)
  * `_includes/layouts/post.njk`: the blog post template (wrapped into `base.njk`)
* `_includes/postlist.njk` is a Nunjucks include and is a reusable component used to display a list of all the posts. `index.njk` has an example of how to use it.