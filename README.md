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

## Releases

| peaceiris/hugo-mod-bulma | jgthms/bulma |
|---|---|
| [v0.2.0](https://github.com/peaceiris/hugo-mod-bulma/releases/tag/v0.2.0) | [0.9.2](https://github.com/jgthms/bulma/releases/tag/0.9.2) |
| [v0.1.2](https://github.com/peaceiris/hugo-mod-bulma/releases/tag/v0.1.2) | [0.9.1](https://github.com/jgthms/bulma/releases/tag/0.9.1) |
