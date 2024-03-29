# rheroicons release history

## rheroicons 1.0.0

This release has number of breaking changes as the Heroicons v2 introduced a new version of the icon library where many icons were renamed. Please see the [Heroicons v2.0.0 release notes](https://github.com/tailwindlabs/heroicons/releases/tag/v2.0.0) for more information.

* Upgraded to Heroicons `v2.0.12` released on 25 October 2022. `v2.0.0` was released on 23 August 2022 which introduced a number of new icons and a new icon style `mini`. Since then, several patches were released. At the time of publication, `v2.0.12` was the latest version.
* The attribute `type` in the `rheroicon` function now accepts `mini`.
* Icon gallery now included option to select `mini` icons. Changes to the layout and styling were also made. In addtion, Webpack was removed from the build process and replaced by Vite.
* Structure of the internal dataset has changed. Before, icons were structured by `<name>$icons$<style>`. The converter was rewritten in python and the structure was changed to `<name>$<style>`. As a result, all functions were updated to align with the new structure.

## rheroicons 0.4.0

* Upgraded to Heroicons `v1.0.6` (released on 02 March 2022) that includes new icons and updates to existing ones.
* Improved error handling in the function `rheroicon`. Missing values or incorrect values throw a warning message rather than stopping the application. This allows the application to continue to run while you test different icons.

## rheroicons 0.3.2

* Upgraded to Heroicons `v1.0` (released on 29 March 2021). This brings fixes to several icons.

## rheroicons 0.3.1

This is a minor package update.

* fixed package descriptions (description, single quotes throughout)
* fixed `launch_gallery` docs (missing `\value`)
* fixed `launch_gallery` example so that it uses `if (interactive())`

## rheroicons 0.3.0

* Prepared package for CRAN submission
* Removed `cli` package as a dependency
* Added tests for `find_icon`
* Revised documentation

## rheroicons 0.2.4

* Upgraded to latest version of Heroicons ([v0.4.2](https://github.com/tailwindlabs/heroicons/releases/tag/v0.4.2))

## rheroicons 0.2.3

This is a minor package update. The main issue was the handling of error messages via the `cli` package. These changes are listed below.

* Updated error message for `rheroicon` function. It now uses {.val {value}}
* Removed error message for find_icons as the default query is "".
* Reset `pkgbump` configuration file

## rheroicons 0.2.21

* The development side of this package now uses Webpack!
* Tested assets in `dev` and `prod` environments using the `dev-app`
* Rebuilt assets
* Updated R package configuration and ignore files

## rheroicons 0.2.2

* Updated to parcel `v2.0`
* Introduced `find_icon` function

## rheroicons 0.2.1

* Restructured static assets for the rheroicons gallery and fixed resource path

## rheroicons 0.2.0

* New package structure! Icons are now generated using the function `rheroicon`. Select an icon using the argument `name`. Icons can be found in the gallery via `launch_gallery()` function. Use the argument `type` to return define the icon style as `outline` or `solid`. Icons can be further customized by passing additional CSS classes using the `classnames` argument.
* Restructured rheroicons gallery as icons are available using an internal dataset. The gallery's client, server, and modules are now located in `R/launch_gallery.R`. Static assets are still located in `inst/rheroicons-demo`.
* Rewrote unit tests

### rheroicons 0.1.6

* Updated to Heroicons `v0.4.0`
* Redesigned icon gallery

### rheroicons 0.1.5

* Restructured `outline` and `solid` icon lists to `icons`. Rendering icon style is now done using the `type` argument. By default, `type = "outline"`.
* Updated gallery to reflect changes with icon styles
* Added unit testing (see `tests/testthat/`)
* Added CI tests
* removed `yarn clean` and rewrote it in `dev/dev.R` as R code

### rheroicons 0.1.4

* Added a `NEWS.md` file to track changes to the package.
* Added Package management directory `dev`. Convert Icons using `dev/dev.R`
