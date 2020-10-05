## hugo-mod-bulma

[Bulma] packaged as a Hugo Module ([Hugo Modules]).

[Bulma]: https://bulma.io/
[Hugo Modules]: https://gohugo.io/hugo-modules/


## Usage

`config/_default/config.yaml`

```yaml
module:
  imports:
    - path: github.com/peaceiris/hugo-mod-bulma
```

`assets/bulma.scss`

```scss
@import "mod/bulma/utilities/_all.sass";
@import "mod/bulma/base/_all.sass";
```

In a Hugo template file.

```html
<head>
  <style>
    {{ $bulmaCSS := resources.Get "bulma.scss" | toCSS | minify }}
    {{ $bulmaCSS.Content | safeCSS }}
  </style>
</head>
```
