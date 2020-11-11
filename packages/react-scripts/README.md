# pelago-react-scripts

This package includes scripts and configuration used by [Create React App](https://github.com/facebook/create-react-app) with custom modifications for Pelago.<br>

## Usage

Replace the `react-scripts` dependency on your respective app's `package.json` file with `pelago-react-scripts` before doing a `yarn install`

## Customizations

- Support dynamic imports for antd component stylesheets
- Replace momentjs with dayjs for antd components that need a datetime library ( eg. DatePicker )
- Add less-loader to support .less and .module.less files

## Third party modules / plugins

- less-loader
- babel-plugin-import
- antd-dayjs-webpack-plugin

## Development setup and workflow

Currently the repo has the following remotes setup

- origin (git@github.com:V287/create-react-app.git) - To keep track of updates made on the repo like any normal repo
- upstream (git@github.com:facebook/create-react-app.git) - To rebase the latest stable release of CRA with master

To rebase with upstream:

- Run `git fetch --tags` to get the latest tags from the respective heads.
- Run `git rebase --onto {latest-tag} {your-branch-name}` and raise a PR.

- If the above doesn't work, try merging the upstream tag with ur feature branch `git merge {latest-tag} {your-branch-name}`

## Releasing

This package has to be bundled and shipped as an npm module. Currently the package is under @sai.mahadevan's account. We will eventually move it to a common pelago account.
