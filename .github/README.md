# scottbrinkmeyer.me

My personal site. Hugo + the Congo theme, deployed on Netlify.

Not much to it - who I am, what I do for work, what I build outside of work, and how to reach me. Posts are optional and there's no schedule.

## What's where

- `content/` - the pages themselves, Markdown with TOML front matter
- `config/_default/` - all site config, split by concern:
  - `hugo.toml` - base URL, theme, pagination, output formats
  - `languages.en.toml` - site title, description, author, social links
  - `menus.en.toml` - the nav
  - `params.toml` - theme options (appearance, search, what shows on articles)
  - `markup.toml`, `taxonomies.toml` - Congo defaults, untouched
- `themes/congo` - git submodule, pinned to a tag. Don't edit in place.
- `netlify.toml` - build command and pinned Hugo version

There is no `layouts/` directory. If I ever need to override a Congo template, copy it out of `themes/congo/layouts/` into a matching path at the repo root.

## Running it locally

The theme is a submodule, so a plain clone leaves `themes/` empty and the build fails. Clone it like this:

    git clone --recurse-submodules https://github.com/sbrinkmeyer/effective-octo-train.git

If it's already cloned without the submodule:

    git submodule update --init --recursive

Then:

    brew install hugo
    hugo server -D

Comes up on http://localhost:1313. The `-D` includes drafts.

To run what Netlify actually runs:

    hugo --gc --minify

## How it deploys

Push to `main`. Netlify picks up the change, builds in a throwaway container, and serves the output from its CDN. Nothing is running anywhere - the container compiles the site to flat files and then goes away. Every deploy is its own immutable snapshot, so rolling back just means pointing at an older build.

Since there's no backend, anything interactive would have to go through a third-party service. Nothing on the site is interactive right now.

Hugo's version is pinned in `netlify.toml`. Congo needs the **extended** build of Hugo.

## Adding something

A new page:

    hugo new content work.md          # then edit content/work.md

A new post:

    hugo new content posts/whatever.md

Front matter starts with `draft = true`. Flip it to `false` when it's ready - that's the only thing standing between a file and it being live.

## Notes to self

- Theme is pinned to a Congo tag, not a moving branch. To update it deliberately: `cd themes/congo && git fetch --tags && git checkout vX.Y.Z`, then rebuild and eyeball it before pushing.
- Post URLs are `/posts/<name>/` and the nav says "Posts" to match.
- Build should be completely silent. Warnings mean something upstream moved.
- Homepage renders `content/_index.md` as written (`params.toml` -> `[homepage] layout`). Switching that to `profile` gives the author-card look instead.
