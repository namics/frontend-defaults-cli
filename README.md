<div align="center">
    <h1>Frontend defaults CLI</h1>
    <p>CLI tool which creates a default setup for your frontend project</p>

[![npm](https://img.shields.io/npm/v/@namics/frontend-defaults-cli.svg)](https://www.npmjs.com/package/@namics/frontend-defaults-cli)
[![Build Status](https://github.com/namics/frontend-defaults-cli/workflows/ci/badge.svg)](https://github.com/namics/frontend-defaults-cli/actions)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](http://opensource.org/licenses/MIT)

</div>
<div style="max-width:640px;margin:0 auto;padding:20px 0 60px 0;">
    <img src="./frontend-defaults-cli.gif" alt="frontend-defaults-cli screencast">
</div>

## Usage

```shell
npx @namics/frontend-defaults-cli my-project
```

or in an existing project

```shell
npx @namics/frontend-defaults-cli
```

### Show potential changes

```shell
npx @namics/frontend-defaults-cli --eslint --dryRun
```

### Example greenfield project default with Typescript

```shell
npx @namics/frontend-defaults-cli my-project --presetTs
```

### Extend existing Typescript project with eslint for typescript

```shell
npx @namics/frontend-defaults-cli --ts --eslint
```

```json
Usage: <project-name> [options]

Options:
  -pTs, --presetTs                Preset typescript (recommended)
  -pEs, --presetEs                Preset javascript
  -ts, --ts                       with typescript configurations
  -es, --es                       with javascript configurations
  -esl, --eslint                  add eslint
  -e --editorconfig               add editorconfig
  -p --prettier                   add prettier
  -s --stylelint                  add stylelint
  -lo --licenseOpenSource         select open source license
  -lc --licenseClosedSource       select closed source license
  -ch --copyrightHolder [string]  for open source license the copyrightHolder is needed
  -gi --gitignore                 add gitignore
  -n --npmrc                      add npmrc
  -r --readme                     add readme file
  -gh --githooks                  add githooks
  -c --commitlint                 add commitlint (will enable githooks too)
  -lch --licenseChecker           add licenseChecker
  -nv --nodeVersion               add node-version file
  -w --webpack                    add webpack with webpack-config-plugins
  -b --build                      add build and watch script
  -i --install                    install dependencies
  -ni --noInstall                 do not install dependencies
  -f --force                      create package.json and override existing files
  -cwd --cwd                      defines where the configurations will be installed (default = process.cwd())
  -d --dryRun                     prints changes will happens by given args
  -h, --help                      output usage information
```

## API usage

```js
const { api } = require('@namics/frontend-defaults-cli');

api({
	ts: true,
	eslint: true,
	install: false,
});
```

## License

[MIT License](./LICENSE)
