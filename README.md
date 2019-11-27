# How to use pre-commit hook

## Prerequisities

You will need a **Snyk account**. Make sure you have one or sign up.

## Installation

Install Snyk CLI using the command `npm install -g snyk`. Once installed, you need to authenticate with your Snyk account. Use the command `snyk auth` and your Snyk acount credentials.

More information on this topic can be found in ofiicial documentation on: https://snyk.io/docs/cli-installation/

Install `pre-commit` package (you can use `brew install pre-commit` command).

## Usage

In your repository edit or create a `.pre-commit-config.yaml` file and configure the pre-commit. This is the basic configuration of this pre-commit hook in your .yaml file:

```
- repo: https://github.com/EconomistDigitalSolutions/cp-precommit-snyk.git
  sha: master
  hooks:
    - id: snyk-audit
```

Install the git hook script using `pre-commit install`. Now `git commit` will automatically run `pre-commit`.

More information in the original documentation on https://pre-commit.com/.
