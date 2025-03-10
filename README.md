# What

This is just a test SFDX project to test SLDS Linter.

## Linter for SLDS (Stylelint)

## Overview
This linter is useful to validate Aura and LWC components. 

### Command-Line Interface (CLI)

To see what all options does slds-linter provide please run `npx @salesforce-ux/slds-linter@latest --help` which gives the below output.
For the first time, it will ask to install the package. Please reply with `y` as yes to install the package.

```
Usage: npx @salesforce-ux/slds-linter@latest [options] [command]

SLDS Linter CLI tool for linting styles and components

Options:
  -V, --version              output the version number
  -h, --help                 display help for command

Commands:
  lint:styles [options]      Run stylelint on all style files
  lint:components [options]  Run eslint on all markup files
  lint [options]             Run both style and component linting
  report [options]           Generate SARIF report from linting results
  emit [options]             Emits the configuration files used by slds-linter cli
  help [command]             display help for command
```

- `npx @salesforce-ux/slds-linter lint` - Runs the ESlint and Stylelint rules on your HTML/CSS/CMP files and outputs issues.
- `npx @salesforce-ux/slds-linter lint:styles` - Runs the Stylelint rules on your CSS files and outputs issues.
- `npx @salesforce-ux/slds-linter lint:components` - Runs the ESlint rules on your HTML/CMP files and outputs issues.
- `npx @salesforce-ux/slds-linter lint --fix`: Attempts to automatically fix violations.
- `npx @salesforce-ux/slds-linter report`: Generates a SARIF report for static analysis.
- `npx @salesforce-ux/slds-linter emit`: Emits the configuration files used by slds-linter cli (defaults to current directory). 

#### Options available with each command

| **Options**              | **Description**                                                              | **Availability**                           |
| ------------------------ | ---------------------------------------------------------------------------- | ------------------------------------------ |
| `-d, --directory <path>` | Target directory to scan (defaults to current directory)                     | lint, lint:styles, lint:components, report |
| `-o, --output <path>`    | Output directory for reports (defaults to current directory)                 | report                                     |
| `--fix`                  | Automatically fix problems                                                   | lint, lint:styles, lint:components         |
| `--config <path>`        | Path to eslint/stylelint config file'         | lint:styles, lint:components               |
| `--config-style <path>`  | Path to stylelint config file'             | lint                                       |
| `--config-eslint <path>` | Path to eslint config file'                    | lint                                       |
| `--editor <editor>`      | Editor to open files with (e.g., vscode, atom, sublime). Defaults to vscode | lint,lint:styles, lint:components          |

These options can also be visualised by using `--help` with each command. For example: Running `npx @salesforce-ux/slds-linter lint --help` will give the options which can be used along with `lint`.
