# External content

MyST Supports cross-referencing into external content in order to create figures and embeds. External content could be in a different version of the AST and would need special handling.


## An External Figure!

![](xref:guide#img:altair-horsepower)

## An External Embed!

:::{embed} xref:guide#img:altair-horsepower
:::

# Local testing

::::{tip} On local testing
:class: dropdown


1. get test source content in `folderA`
  * myst start --execute --headless
  * content server running on `localhost:3100`
2. start myst-theme e.g. `npm run theme:book`
  * theme running on `localhost:3000`
3. get second set of test content in `folderB`
  * add `local: http://localhost:3000` to `myst.yml#project.references`
  * add external cross references and embeds in `folderB` pointing to the local content in `folderA`
  * `myst start --execute --headless`
  * content server running on `localhost:3101`
4. in a second `myst-theme` folder, or without fully restarting the theme from step 2
  * add a `.env` file to `themes/book`
  * add `CONTENT_CDN_PORT=3101`
  * `npm run theme:book`
  * theme running on `localhost:3001`
  * test this website 👆

::::

## A local embed (shorthand)

![](xref:local#out:simple-matplotlib)

## a local embed

:::{embed} xref:local#out:simple-matplotlib
:::

## cross references

* [To a notebook cell](xref:local#out:simple-matplotlib)
* [To a figure](xref:local#fig:simple-matplotlib)