[![logo][]](https://xylabs.com)

# @xylabs/action-code-climate-test-reporter

## Table of Contents

- [@xylabs/action-code-climate-test-reporter](#xylabsaction-code-climate-test-reporter)
  - [Table of Contents](#table-of-contents)
  - [Description](#description)
  - [Usage](#usage)
  - [Maintainers](#maintainers)
  - [License](#license)
  - [Credits](#credits)

## Description

Containerized version of CodeClimate Test Reporter for use as a GitHub action.

## Usage

Formatting code coverage:

```yaml
- name: format code coverage
  uses: ./.github/actions/cc-test-reporter
  with:
    subcommand: "format-coverage -t lcov ./coverage/lcov.info"

```

Uploading code coverage:

```yaml
- name: upload code coverage
  uses: ./.github/actions/cc-test-reporter
  env:
    CC_TEST_REPORTER_ID: ${{ secrets.CC_TEST_REPORTER_ID }}
  with:
    subcommand: "upload-coverage"
```


## Maintainers

-   [Arie Trouw](https://github.com/arietrouw) (<https://arietrouw.com>)

## License

See the [LICENSE](LICENSE) file for license details

## Credits

[Made with 🔥 and ❄️ by XY Labs](https://xylabs.com)

[logo]: https://cdn.xy.company/img/brand/XYPersistentCompany_Logo_Icon_Colored.svg
