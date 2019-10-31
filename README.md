# Kibana Plugin Tutorial
A not so comprehensive tutorial on Kibana Plugin. Please contribute.

## Menu
- Development environment setup
- References
- Changing the logo in Loader


## Development environment

Before we proceed, ensure you have Kibana development environment setup. 
For Version 7.4, you can find it below
https://github.com/elastic/kibana/blob/7.4/CONTRIBUTING.md#development-environment-setup

Use kibana plugin generator which is available at https://github.com/elastic/kibana/tree/7.4/packages/kbn-plugin-generator

### Quick Start

To target the current development version of Kibana just use the default  `master` branch.

```sh
node scripts/generate_plugin my_plugin_name
# generates a plugin in `plugins/my_plugin_name`
```


```sh
git checkout 7.4
yarn kbn bootstrap # always bootstrap when switching branches
node scripts/generate_plugin my_plugin_name
# generates a plugin for Kibana 7.4 in `./plugins/my_plugin_name`
```

The generate script supports a few flags; run it with the `--help` flag to learn more.

```sh
node scripts/generate_plugin --help
```

### Development

See the [kibana contributing guide](https://github.com/elastic/kibana/blob/master/CONTRIBUTING.md) for instructions setting up your development environment. Once you have completed that, use the following yarn scripts.

  - `yarn kbn bootstrap`

    Install dependencies and crosslink Kibana and all projects/plugins.

    > ***IMPORTANT:*** Use this script instead of `yarn` to install dependencies when switching branches, and re-run it whenever your dependencies change.

  - `yarn start`

    Start kibana and have it include this plugin. You can pass any arguments that you would normally send to `bin/kibana`

      ```
      yarn start --elasticsearch.hosts http://localhost:9220
      ```

  - `yarn build`

    Build a distributable archive of your plugin.

  - `yarn test:browser`

    Run the browser tests in a real web browser.

  - `yarn test:mocha`

    Run the server tests using mocha.

For more information about any of these commands run `yarn ${task} --help`. For a full list of tasks checkout the `package.json` file, or run `yarn run`.


## References
- https://www.elastic.co/guide/en/kibana/current/plugin-development.html
- 
