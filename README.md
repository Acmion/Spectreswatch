# Spectreswatch https://spectreswatch.acmion.com

Themes for [Spectre.css](https://picturepan2.github.io/spectre/), inspired by [Bulmaswatch](https://jenil.github.io/bulmaswatch/) and [Bootswatch](https://bootswatch.com). See previews at https://spectreswatch.acmion.com.

**Note:** Only one customized theme has been created at this time. 

## Spectre.css

The repository for [Spectre.css](https://github.com/picturepan2/spectre) contains lots of useful information on building and customizing your copy of Spectre. Use that as a reference.

## Key Changes

1. Introduced the class `content`, which acts like the container in, for example, Bulma.
2. Changed colors.
3. Changed size variables.
4. Changed HTML font size from 20px to 10px, to make rem calculations more natural.
5. Doubled all rem units (due to the halving of HTML font size), except the units of the `<select>` element `background` property.
6. Created CSS variable declarations of some SCSS variables.

## How Can I Apply the Theming of Spectreswatch to Another Copy of Spectre.css?

1. Clone Spectreswatch.
2. Choose a theme.
3. Copy the files:
    - `theme-name/src/_variables.scss`
    - `theme-name/src/_x-overrides.scss`
    - `theme-name/src/_x-overrides-exp.scss`
4. Clone Spectre (or get the source in some other way).
4. In your Spectre do the following:
    - Paste the copied files in the `src/` directory.
    - In `src/spectre.scss`, on the last row, import the changes with: `@import "x-overrides";` 
    - In `src/spectre-exp.scss`, on the last row, import the changes with: `@import "x-overrides-exp";` 
    - Replace all instances of `rem` with `rem * 2` in all `.scss` files. 
5. Compile Spectre according to the instructions in the main Spectre repository.
6. Done.

You might also want to change some CSS that affects the Spectre docs pages (not necessary):

1. Copy `Spectreswatch/theme-name/docs/src/_x-docs.scss` and paste it in your `path-to-your-spectre/docs/src/_x-docs.scss`.
2. In `path-to-your-spectre/docs/src/docs.scss`, on the last row, import the changes with: `@import "x-docs";`.
3. Done. 

## Credits 

- [picturepan2](https://github.com/picturepan2/) for [Spectre](https://picturepan2.github.io/spectre/)
- [thomaspark](https://github.com/thomaspark/) for [Bootswatch](https://bootswatch.com/)
- [jenil](github.com/jenil/) for [Bulmaswatch](https://jenil.github.io/bulmaswatch/)

## License

MIT