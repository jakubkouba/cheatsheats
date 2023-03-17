# Ruby and Rails cheet sheet

## gem installation

### Bundler

#### Addding flags to for gem installation
`bundkle config build.{gem-name} --with-cflags ...`

### Build with native extension issues

#### Macro expansion

Error: `error: '(' and '{' tokens introducing statement expression appear in different macro expansion contexts [-Werror,-Wcompound-token-split-by-macro]`

Sollution: `--with-cppflags="-Wno-compound-token-split-by-macro"`

#### Shifting negative signe value

Error: `error: shifting a negative signed value is undefined [-Werror,-Wshift-negative-value]`

Sollution: `--with-cppflags="-D_FORTIFY_SOURCE=0 -Wno-shift-negative-value`

## Runnig rails app

:point_right: Make sure you have SECRET_KEY_BASE set
