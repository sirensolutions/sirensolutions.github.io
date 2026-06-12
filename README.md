# sirensolutions.github.io

Source for the [Siren plugins documentation site](https://sirensolutions.github.io), built with [Jekyll](https://jekyllrb.com) and hosted on GitHub Pages.

## Prerequisites

- **Ruby** (3.1.x recommended) — managed via [rbenv](https://github.com/rbenv/rbenv) or [RVM](https://rvm.io). A `.ruby-version` file is included and pins the version to 3.1.3.
- **Bundler** — install with `gem install bundler`
- **Homebrew** (macOS) — required to install system dependencies like `gmp`

> **macOS Apple Silicon note:** Ruby must be compiled for `arm64`. If you get a `Library not loaded: .../libgmp.10.dylib` error, your Ruby was built against the Intel Homebrew path (`/usr/local`). Install a fresh Ruby via rbenv to get a native arm64 build.

Confirm that the ruby version is getting picked from rbenv by doing `which ruby`. If it says something other than `$HOME/.rbenv/shims/ruby`, then run `eval "$(rbenv init - bash)"` and try `which ruby` again. If you are using .zshrc on MacOS, run `eval "$(rbenv init - zsh)"`

The `ruby -v` version should match the version in the .ruby-version file.

## Running locally

1. **Install dependencies**

   ```bash
   bundle install
   ```

2. **Start the development server**

   ```bash
   bundle exec jekyll serve
   ```

3. Open [http://localhost:4000](http://localhost:4000) in your browser.

   The site rebuilds automatically when you save changes.

## Useful flags

| Flag | Description |
|---|---|
| `--livereload` | Automatically reload the browser on changes |
| `--incremental` | Only rebuild changed pages (faster for large sites) |
| `--drafts` | Include posts in `_drafts/` |

Example:

```bash
bundle exec jekyll serve --livereload
```

## Further reading

- [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll) — official GitHub guide
- [Jekyll documentation](https://jekyllrb.com/docs/)
