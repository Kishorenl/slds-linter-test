What

This is just a test SFDX project to test SLDS Linter.

How

- Install the required linter plugin

```
npm i @salesforce-ux/slds-linter
```

- Copy the required scripts into package.json `scripts` section

Here are all the scripts that are needed.

```
    "lint:styles": "stylelint \"./**/*.css\" --config=.stylelintrc.yml",
    "lint:components": "eslint \"**/*.{html,cmp}\" --ext .html,.cmp --config=.eslintrc.yml",
    "slds:lint": "npm run lint:components; npm run lint:styles",
    "fix": "stylelint \"**/*.css\" -c .stylelintrc.yml --fix ",
    "report": "node node_modules/@salesforce-ux/stylelint-plugin-slds/build/report.js force-app/ -c .stylelintrc.yml",
    "setup-lint": "node ./node_modules/@salesforce-ux/slds-linter/build/setup.js"

```

- Setup the required configurations

```
npm run setup-lint
```

Now you should be able to run any of the below commands based on your intent -

To get all the validation results

```
npm run slds:lint
```

To auto-fix some of the rules

```
npm run fix
```

To run a .json or .sarif report of the validation results

```
npm run report
```
