# ABC - Absorb Chaos - Release Potential

Fancy new [website for Absorbing Chaos](https://absorbingchaos.com). This has gone through quite a few iterations, but it's time to try something new *and actually publish it this time!*

## Development

[Hugo](https://gohugo.io/) using a forked version of the [Sawmill theme](https://github.com/forestryio/sawmill) located in [the abc-sawmill](https://github.com/AbsorbingChaos/abc-sawmill) repository.

## Deployment

[GitHub Actions](https://github.com/features/actions) and [Cloudflare Workers](https://workers.cloudflare.com/).

## Theme Development

2018/04/20 theme announcement / blog post: [Sawmill: A Razor-sharp Layout Composer for Hugo and Forestry](https://forestry.io/blog/sawmill-layout-composer-for-hugo-and-forestry/#/)

This theme uses Webpack to compile assets.

After cloning the theme, run `npm install` to install the necessary dependencies. Run `npm run watch` to watch and live-compile assets, and run `npm run prod` to build production assets.

Assets should be compiled for production and committed to repo when committing css/js updates.

Source files are located in the `assets` folder and compiled to the `static` folder.

### Brand Color

When writing styles that utilize the customizable brand color, add them to `layouts/partials/brand_css.html` instead of to the `.scss` files. Since the brand color should be customizable without having to directly modify the theme or re-run the build scripts, the relevant styles are embedded in the html document to take advantage of settings saved in the site's `config.toml`.
