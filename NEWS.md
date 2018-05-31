# pkgdown 1.0.0.9000

* Multi-page Changelogs (generated from `NEWS.md` by setting `news: one_page:
  false` in _pkgdown.yml) are now rendered correctly.

* CITATION files with non-UTF-8 encodings (latin1) no longer generate an error.
  For non-UTF-8 locales, ensure you have e.g. `Encoding: latin1` in your `DESCRIPTION`
  (#689).

* The Algolia logo was restored in search results (#673)

* Suppress web indexing by setting `noindex: true` under `template:params`
  in `pkgdown.yml` (#686)

* Markdown files (e.g., `CODE_OF_CONDUCT.md`) stored in `.github/` are now copied and
  linked correctly (#682).

* `build_article()` now sets `IN_PKGDOWN` env var so `in_pkgdown()` works 
  (#650).

* Default navbar template now correctly uses site title, not package name 
  (the package name is the default title, so this will not affect most sites) 
  (#654).

* Auto-linking of calls to `vignette()` is now more robust to calls that 
  don't actually link to vignettes (#652).

* `pkgdown.js` is now better isolated so it should still work even if you 
  load html widgets that import a different version of jquery (#655).

* `\Sexpr{}` now supports `results=text`, `results=Rd` and `results=hide` (#651).

* Empty sections are now ignored (#656). Previously, empty sections caused 
  error `Error in rep(TRUE, length(x) - 1)`.

* `\tabular{}` now longer requires a terminal `\cr` (#664, #645).

* Added a keyboard shortcut for searching. Press `shift` + `/` to move focus
  to the search bar (#642)
 
* Infix functions (like `%+%`) now show as `` `%+%` ``, not 
  `` `%+%`() `` on reference index (#659).

* Support re-exported non-function objects (#666, #669).

* Improved display for icons - icons now must be 30px and are embedded in 
  separate column of reference index table (instead of being inside 
  a comment!) (#607).
  
* Add `inst/pkgdown.yml` as a possible site configuration file so that packages on 
  CRAN can be built without needing the development version (#662).

# pkgdown 1.0.0

* Major refactoring of path handling. `build_` functions no longer take
  `path` or `depth` arguments. Instead, set the `destination` directory 
  at the top level of `pkgdown.yml`.

* Similarly, `build_news()` no longer takes a `one_page` argument;
  this should now be specified in the `_pkgdown.yml` instead. See the 
  documentation for an example.
