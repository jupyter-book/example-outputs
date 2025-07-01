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

1. Get test source content in `folderA`
   `myst start --execute --headless` starts a content server running on `localhost:3100`.
2. Start `myst-theme`
   `npm run theme:book` in the MyST Theme repository, e.g. `npm run theme:book` starts a theme running on `localhost:3000`.
3. Get second set of test content in `folderB`
   1. Add `local: http://localhost:3000` to `myst.yml#project.references`.
   2. Add external cross references and embeds in `folderB` pointing to the local content in `folderA`.
   3. Start a second content server with `myst start --execute --headless`, which runs on `localhost:3101`.
4. In a second `myst-theme` folder, or without fully restarting the theme from step 2.
   - Set `CONTENT_CDN_PORT=3101` in your environment, and run another MyST Theme process (see (2))
5. Test this website 👆.

::::

## A local embed (shorthand)

![](xref:local#out:simple-matplotlib)

## a local embed

:::{embed} xref:local#out:simple-matplotlib
:::

## cross references

- [To a notebook cell](xref:local#out:simple-matplotlib)
- [To a figure](xref:local#fig:simple-matplotlib)
