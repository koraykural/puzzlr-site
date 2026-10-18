# Fonts

The app's own fonts, cut down to Latin and Turkish letters and served from
this site so the pages make no request to a font service.

- `nunito.woff2`: Nunito. Copyright 2014 The Nunito Project Authors
  (https://github.com/googlefonts/nunito).
- `baloo2.woff2`: Baloo 2. Copyright 2019 The Baloo 2 Project Authors
  (https://github.com/EkType/Baloo2).

Both are licensed under the SIL Open Font License, Version 1.1
(https://openfontlicense.org). The licence text is also kept inside each file.

Rebuilt from the app's `assets/fonts/*.ttf` with fontTools:

```sh
pyftsubset Nunito.ttf --unicodes="U+0000-00FF,U+0100-017F,U+2018-201F,U+2022,U+2026,U+20BA" \
  --layout-features='*' --name-IDs='*' --name-languages='*' \
  --flavor=woff2 --output-file=nunito.woff2
```
