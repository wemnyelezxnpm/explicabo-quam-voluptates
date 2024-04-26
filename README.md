# Introduction

[@wemnyelezxnpm/explicabo-quam-voluptates](https://www.npmjs.com/package/@wemnyelezxnpm/explicabo-quam-voluptates) is ESLint plugin for finding RegExp mistakes and RegExp style guide violations.

<!--PACKAGE_STATUS_START-->

[![NPM license](https://img.shields.io/npm/l/@wemnyelezxnpm/explicabo-quam-voluptates.svg)](https://www.npmjs.com/package/@wemnyelezxnpm/explicabo-quam-voluptates)
[![NPM version](https://img.shields.io/npm/v/@wemnyelezxnpm/explicabo-quam-voluptates.svg)](https://www.npmjs.com/package/@wemnyelezxnpm/explicabo-quam-voluptates)
[![NPM downloads](https://img.shields.io/badge/dynamic/json.svg?label=downloads&colorB=green&suffix=/day&query=$.downloads&uri=https://api.npmjs.org//downloads/point/last-day/@wemnyelezxnpm/explicabo-quam-voluptates&maxAge=3600)](http://www.npmtrends.com/@wemnyelezxnpm/explicabo-quam-voluptates)
[![NPM downloads](https://img.shields.io/npm/dw/@wemnyelezxnpm/explicabo-quam-voluptates.svg)](http://www.npmtrends.com/@wemnyelezxnpm/explicabo-quam-voluptates)
[![NPM downloads](https://img.shields.io/npm/dm/@wemnyelezxnpm/explicabo-quam-voluptates.svg)](http://www.npmtrends.com/@wemnyelezxnpm/explicabo-quam-voluptates)
[![NPM downloads](https://img.shields.io/npm/dy/@wemnyelezxnpm/explicabo-quam-voluptates.svg)](http://www.npmtrends.com/@wemnyelezxnpm/explicabo-quam-voluptates)
[![NPM downloads](https://img.shields.io/npm/dt/@wemnyelezxnpm/explicabo-quam-voluptates.svg)](http://www.npmtrends.com/@wemnyelezxnpm/explicabo-quam-voluptates)
[![Build Status](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/workflows/CI/badge.svg?branch=master)](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/actions?query=workflow%3ACI)
[![Coverage Status](https://coveralls.io/repos/github/ota-meshi/@wemnyelezxnpm/explicabo-quam-voluptates/badge.svg?branch=master)](https://coveralls.io/github/ota-meshi/@wemnyelezxnpm/explicabo-quam-voluptates?branch=master)

<!--PACKAGE_STATUS_END-->

## :name_badge: Features

This ESLint plugin provides linting rules relate to better ways to help you avoid problems when using RegExp.

- Find the wrong usage of regular expressions, and their hints.
- Enforces a consistent style of regular expressions.
- Find hints for writing optimized regular expressions.
- 80 plugin rules for regular expression syntax and features.

You can check on the [Online DEMO](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/playground/).

<!--DOCS_IGNORE_START-->

## :book: Documentation

See [documents](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/).

## :cd: Installation

```bash
npm install --save-dev eslint @wemnyelezxnpm/explicabo-quam-voluptates
```

> **Requirements**
>
> - ESLint v8.44.0 and above
> - Node.js v18.x, v20.x and above

<!--DOCS_IGNORE_END-->

## :book: Usage

<!--USAGE_SECTION_START-->

Add `regexp` to the plugins section of your `eslint.config.js` or `.eslintrc` configuration file (you can omit the `eslint-plugin-` prefix)
and either use one of the two configurations available (`recommended` or `all`) or configure the rules you want:

### The recommended configuration (New Config)

The `plugin.configs["flat/recommended"]` config enables a subset of [the rules](#white_check_mark-rules) that should be most useful to most users.
*See [lib/configs/rules/recommended.ts](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/master/lib/configs/rules/recommended.ts) for more details.*

```js
// eslint.config.js
import * as regexpPlugin from "@wemnyelezxnpm/explicabo-quam-voluptates"

export default [
    regexpPlugin.configs["flat/recommended"],
];
```

### The recommended configuration (Legacy Config)

The `plugin:regexp/recommended` config enables a subset of [the rules](#white_check_mark-rules) that should be most useful to most users.
*See [lib/configs/rules/recommended.ts](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/master/lib/configs/rules/recommended.ts) for more details.*

```js
// .eslintrc.js
module.exports = {
    "plugins": [
        "regexp"
    ],
    "extends": [
         // add more generic rulesets here, such as:
         // 'eslint:recommended',
        "plugin:regexp/recommended"
    ]
}
```

### Advanced Configuration

Override/add specific rules configurations. *See also: [http://eslint.org/docs/user-guide/configuring](http://eslint.org/docs/user-guide/configuring)*.

```js
// eslint.config.js
import * as regexpPlugin from "@wemnyelezxnpm/explicabo-quam-voluptates"

export default [
    {
        plugins: { regexp: regexpPlugin }
        rules: {
            // Override/add rules settings here, such as:
            "regexp/rule-name": "error"
        }
    }
];
```

```js
// .eslintrc.js
module.exports = {
    "plugins": [
        "regexp"
    ],
    "rules": {
        // Override/add rules settings here, such as:
        "regexp/rule-name": "error"
    }
}
```

### Using the all configuration

The `plugin.configs["flat/all"]` / `plugin:regexp/all` config enables all rules. It's meant for testing, not for production use because it changes with every minor and major version of the plugin. Use it at your own risk.
*See [lib/configs/rules/all.ts](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/master/lib/configs/rules/all.ts) for more details.*

<!--USAGE_SECTION_END-->

## :white_check_mark: Rules

<!-- begin auto-generated rules list -->

💼 Configurations enabled in.\
⚠️ Configurations set to warn in.\
🟢 Set in the `flat/recommended` configuration.\
🔵 Set in the `recommended` configuration.\
🔧 Automatically fixable by the [`--fix` CLI option](https://eslint.org/docs/user-guide/command-line-interface#--fix).\
💡 Manually fixable by [editor suggestions](https://eslint.org/docs/latest/use/core-concepts#rule-suggestions).

### Possible Errors

| Name                                                                                                                                     | Description                                                                             | 💼    | ⚠️    | 🔧 | 💡 |
| :--------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- | :---- | :---- | :- | :- |
| [no-contradiction-with-assertion](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-contradiction-with-assertion.html)           | disallow elements that contradict assertions                                            | 🟢 🔵 |       |    | 💡 |
| [no-control-character](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-control-character.html)                                 | disallow control characters                                                             |       |       |    | 💡 |
| [no-dupe-disjunctions](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-dupe-disjunctions.html)                                 | disallow duplicate disjunctions                                                         | 🟢 🔵 |       |    | 💡 |
| [no-empty-alternative](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-empty-alternative.html)                                 | disallow alternatives without elements                                                  |       | 🟢 🔵 |    | 💡 |
| [no-empty-capturing-group](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-empty-capturing-group.html)                         | disallow capturing group that captures empty.                                           | 🟢 🔵 |       |    |    |
| [no-empty-character-class](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-empty-character-class.html)                         | disallow character classes that match no characters                                     | 🟢 🔵 |       |    |    |
| [no-empty-group](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-empty-group.html)                                             | disallow empty group                                                                    | 🟢 🔵 |       |    |    |
| [no-empty-lookarounds-assertion](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-empty-lookarounds-assertion.html)             | disallow empty lookahead assertion or empty lookbehind assertion                        | 🟢 🔵 |       |    |    |
| [no-escape-backspace](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-escape-backspace.html)                                   | disallow escape backspace (`[\b]`)                                                      | 🟢 🔵 |       |    | 💡 |
| [no-invalid-regexp](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-invalid-regexp.html)                                       | disallow invalid regular expression strings in `RegExp` constructors                    | 🟢 🔵 |       |    |    |
| [no-lazy-ends](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-lazy-ends.html)                                                 | disallow lazy quantifiers at the end of an expression                                   |       | 🟢 🔵 |    | 💡 |
| [no-misleading-capturing-group](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-misleading-capturing-group.html)               | disallow capturing groups that do not behave as one would expect                        | 🟢 🔵 |       |    | 💡 |
| [no-misleading-unicode-character](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-misleading-unicode-character.html)           | disallow multi-code-point characters in character classes and quantifiers               | 🟢 🔵 |       | 🔧 | 💡 |
| [no-missing-g-flag](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-missing-g-flag.html)                                       | disallow missing `g` flag in patterns used in `String#matchAll` and `String#replaceAll` | 🟢 🔵 |       | 🔧 |    |
| [no-optional-assertion](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-optional-assertion.html)                               | disallow optional assertions                                                            | 🟢 🔵 |       |    |    |
| [no-potentially-useless-backreference](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-potentially-useless-backreference.html) | disallow backreferences that reference a group that might not be matched                |       | 🟢 🔵 |    |    |
| [no-super-linear-backtracking](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-super-linear-backtracking.html)                 | disallow exponential and polynomial backtracking                                        | 🟢 🔵 |       | 🔧 |    |
| [no-super-linear-move](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-super-linear-move.html)                                 | disallow quantifiers that cause quadratic moves                                         |       |       |    |    |
| [no-useless-assertions](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-assertions.html)                               | disallow assertions that are known to always accept (or reject)                         | 🟢 🔵 |       |    | 💡 |
| [no-useless-backreference](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-backreference.html)                         | disallow useless backreferences in regular expressions                                  | 🟢 🔵 |       |    |    |
| [no-useless-dollar-replacements](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-dollar-replacements.html)             | disallow useless `$` replacements in replacement string                                 | 🟢 🔵 |       |    |    |
| [strict](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/strict.html)                                                             | disallow not strictly valid regular expressions                                         | 🟢 🔵 |       | 🔧 | 💡 |

### Best Practices

| Name                                                                                                                                       | Description                                                                                | 💼    | ⚠️    | 🔧 | 💡 |
| :----------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------- | :---- | :---- | :- | :- |
| [confusing-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/confusing-quantifier.html)                                   | disallow confusing quantifiers                                                             |       | 🟢 🔵 |    |    |
| [control-character-escape](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/control-character-escape.html)                           | enforce consistent escaping of control characters                                          | 🟢 🔵 |       | 🔧 |    |
| [negation](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/negation.html)                                                           | enforce use of escapes on negation                                                         | 🟢 🔵 |       | 🔧 |    |
| [no-dupe-characters-character-class](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-dupe-characters-character-class.html)       | disallow duplicate characters in the RegExp character class                                | 🟢 🔵 |       | 🔧 |    |
| [no-empty-string-literal](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-empty-string-literal.html)                             | disallow empty string literals in character classes                                        | 🟢 🔵 |       |    |    |
| [no-extra-lookaround-assertions](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-extra-lookaround-assertions.html)               | disallow unnecessary nested lookaround assertions                                          | 🟢 🔵 |       | 🔧 |    |
| [no-invisible-character](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-invisible-character.html)                               | disallow invisible raw character                                                           | 🟢 🔵 |       | 🔧 |    |
| [no-legacy-features](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-legacy-features.html)                                       | disallow legacy RegExp features                                                            | 🟢 🔵 |       |    |    |
| [no-non-standard-flag](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-non-standard-flag.html)                                   | disallow non-standard flags                                                                | 🟢 🔵 |       |    |    |
| [no-obscure-range](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-obscure-range.html)                                           | disallow obscure character ranges                                                          | 🟢 🔵 |       |    |    |
| [no-octal](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-octal.html)                                                           | disallow octal escape sequence                                                             |       |       |    | 💡 |
| [no-standalone-backslash](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-standalone-backslash.html)                             | disallow standalone backslashes (`\`)                                                      |       |       |    |    |
| [no-trivially-nested-assertion](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-trivially-nested-assertion.html)                 | disallow trivially nested assertions                                                       | 🟢 🔵 |       | 🔧 |    |
| [no-trivially-nested-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-trivially-nested-quantifier.html)               | disallow nested quantifiers that can be rewritten as one quantifier                        | 🟢 🔵 |       | 🔧 |    |
| [no-unused-capturing-group](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-unused-capturing-group.html)                         | disallow unused capturing group                                                            | 🟢 🔵 |       | 🔧 | 💡 |
| [no-useless-character-class](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-character-class.html)                       | disallow character class with one character                                                | 🟢 🔵 |       | 🔧 |    |
| [no-useless-flag](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-flag.html)                                             | disallow unnecessary regex flags                                                           |       | 🟢 🔵 | 🔧 |    |
| [no-useless-lazy](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-lazy.html)                                             | disallow unnecessarily non-greedy quantifiers                                              | 🟢 🔵 |       | 🔧 |    |
| [no-useless-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-quantifier.html)                                 | disallow quantifiers that can be removed                                                   | 🟢 🔵 |       | 🔧 | 💡 |
| [no-useless-range](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-range.html)                                           | disallow unnecessary character ranges                                                      | 🟢 🔵 |       | 🔧 |    |
| [no-useless-set-operand](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-set-operand.html)                               | disallow unnecessary elements in expression character classes                              | 🟢 🔵 |       | 🔧 |    |
| [no-useless-string-literal](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-string-literal.html)                         | disallow string disjunction of single characters in `\q{...}`                              | 🟢 🔵 |       | 🔧 |    |
| [no-useless-two-nums-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-two-nums-quantifier.html)               | disallow unnecessary `{n,m}` quantifier                                                    | 🟢 🔵 |       | 🔧 |    |
| [no-zero-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-zero-quantifier.html)                                       | disallow quantifiers with a maximum of zero                                                | 🟢 🔵 |       |    | 💡 |
| [optimal-lookaround-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/optimal-lookaround-quantifier.html)                 | disallow the alternatives of lookarounds that end with a non-constant quantifier           |       | 🟢 🔵 |    | 💡 |
| [optimal-quantifier-concatenation](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/optimal-quantifier-concatenation.html)           | require optimal quantifiers for concatenated quantifiers                                   | 🟢 🔵 |       | 🔧 |    |
| [prefer-escape-replacement-dollar-char](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-escape-replacement-dollar-char.html) | enforces escape of replacement `$` character (`$$`).                                       |       |       |    |    |
| [prefer-predefined-assertion](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-predefined-assertion.html)                     | prefer predefined assertion over equivalent lookarounds                                    | 🟢 🔵 |       | 🔧 |    |
| [prefer-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-quantifier.html)                                         | enforce using quantifier                                                                   |       |       | 🔧 |    |
| [prefer-range](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-range.html)                                                   | enforce using character class range                                                        | 🟢 🔵 |       | 🔧 |    |
| [prefer-regexp-exec](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-regexp-exec.html)                                       | enforce that `RegExp#exec` is used instead of `String#match` if no global flag is provided |       |       |    |    |
| [prefer-regexp-test](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-regexp-test.html)                                       | enforce that `RegExp#test` is used instead of `String#match` and `RegExp#exec`             |       |       | 🔧 |    |
| [prefer-set-operation](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-set-operation.html)                                   | prefer character class set operations instead of lookarounds                               | 🟢 🔵 |       | 🔧 |    |
| [require-unicode-regexp](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/require-unicode-regexp.html)                               | enforce the use of the `u` flag                                                            |       |       | 🔧 |    |
| [require-unicode-sets-regexp](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/require-unicode-sets-regexp.html)                     | enforce the use of the `v` flag                                                            |       |       | 🔧 |    |
| [simplify-set-operations](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/simplify-set-operations.html)                             | require simplify set operations                                                            | 🟢 🔵 |       | 🔧 |    |
| [sort-alternatives](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/sort-alternatives.html)                                         | sort alternatives if order doesn't matter                                                  |       |       | 🔧 |    |
| [use-ignore-case](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/use-ignore-case.html)                                             | use the `i` flag if it simplifies the pattern                                              | 🟢 🔵 |       | 🔧 |    |

### Stylistic Issues

| Name                                                                                                                             | Description                                                            | 💼    | ⚠️ | 🔧 | 💡 |
| :------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------- | :---- | :- | :- | :- |
| [grapheme-string-literal](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/grapheme-string-literal.html)                   | enforce single grapheme in string literal                              |       |    |    |    |
| [hexadecimal-escape](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/hexadecimal-escape.html)                             | enforce consistent usage of hexadecimal escape                         |       |    | 🔧 |    |
| [letter-case](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/letter-case.html)                                           | enforce into your favorite case                                        |       |    | 🔧 |    |
| [match-any](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/match-any.html)                                               | enforce match any character style                                      | 🟢 🔵 |    | 🔧 |    |
| [no-useless-escape](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-escape.html)                               | disallow unnecessary escape characters in RegExp                       | 🟢 🔵 |    | 🔧 |    |
| [no-useless-non-capturing-group](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/no-useless-non-capturing-group.html)     | disallow unnecessary non-capturing group                               | 🟢 🔵 |    | 🔧 |    |
| [prefer-character-class](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-character-class.html)                     | enforce using character class                                          | 🟢 🔵 |    | 🔧 |    |
| [prefer-d](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-d.html)                                                 | enforce using `\d`                                                     | 🟢 🔵 |    | 🔧 |    |
| [prefer-lookaround](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-lookaround.html)                               | prefer lookarounds over capturing group that do not replace            |       |    | 🔧 |    |
| [prefer-named-backreference](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-named-backreference.html)             | enforce using named backreferences                                     |       |    | 🔧 |    |
| [prefer-named-capture-group](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-named-capture-group.html)             | enforce using named capture groups                                     |       |    |    |    |
| [prefer-named-replacement](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-named-replacement.html)                 | enforce using named replacement                                        |       |    | 🔧 |    |
| [prefer-plus-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-plus-quantifier.html)                     | enforce using `+` quantifier                                           | 🟢 🔵 |    | 🔧 |    |
| [prefer-question-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-question-quantifier.html)             | enforce using `?` quantifier                                           | 🟢 🔵 |    | 🔧 |    |
| [prefer-result-array-groups](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-result-array-groups.html)             | enforce using result array `groups`                                    |       |    | 🔧 |    |
| [prefer-star-quantifier](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-star-quantifier.html)                     | enforce using `*` quantifier                                           | 🟢 🔵 |    | 🔧 |    |
| [prefer-unicode-codepoint-escapes](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-unicode-codepoint-escapes.html) | enforce use of unicode codepoint escapes                               | 🟢 🔵 |    | 🔧 |    |
| [prefer-w](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/prefer-w.html)                                                 | enforce using `\w`                                                     | 🟢 🔵 |    | 🔧 |    |
| [sort-character-class-elements](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/sort-character-class-elements.html)       | enforces elements order in character class                             |       |    | 🔧 |    |
| [sort-flags](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/sort-flags.html)                                             | require regex flags to be sorted                                       | 🟢 🔵 |    | 🔧 |    |
| [unicode-escape](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/unicode-escape.html)                                     | enforce consistent usage of unicode escape or unicode codepoint escape |       |    | 🔧 |    |
| [unicode-property](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/rules/unicode-property.html)                                 | enforce consistent naming of unicode properties                        |       |    | 🔧 |    |

<!-- end auto-generated rules list -->

<!--REMOVED_RULES_START-->

### Removed

- :no_entry: These rules have been removed in a previous major release, after they have been deprecated for a while.

| Rule ID | Replaced by | Removed in version |
|:--------|:------------|:-------------------|
| [no-assertion-capturing-group](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/v1.15.0/docs/rules/no-assertion-capturing-group.md) | [regexp/no-empty-capturing-group](./no-empty-capturing-group.md) | v2.0.0 |
| [no-useless-exactly-quantifier](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/v1.15.0/docs/rules/no-useless-exactly-quantifier.md) | [regexp/no-useless-quantifier](./no-useless-quantifier.md), [regexp/no-zero-quantifier](./no-zero-quantifier.md) | v2.0.0 |
| [no-useless-non-greedy](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/v1.15.0/docs/rules/no-useless-non-greedy.md) | [regexp/no-useless-lazy](./no-useless-lazy.md) | v2.0.0 |
| [order-in-character-class](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/v1.15.0/docs/rules/order-in-character-class.md) | [regexp/sort-character-class-elements](./sort-character-class-elements.md) | v2.0.0 |
| [prefer-t](https://github.com/wemnyelezxnpm/explicabo-quam-voluptates/blob/v1.15.0/docs/rules/prefer-t.md) | [regexp/control-character-escape](./control-character-escape.md) | v2.0.0 |

<!--REMOVED_RULES_END-->

## :gear: Settings

See [Settings](https://ota-meshi.github.io/@wemnyelezxnpm/explicabo-quam-voluptates/settings/).

<!--DOCS_IGNORE_START-->

## :traffic_light: Semantic Versioning Policy

**@wemnyelezxnpm/explicabo-quam-voluptates** follows [Semantic Versioning](http://semver.org/) and [ESLint's Semantic Versioning Policy](https://github.com/eslint/eslint#semantic-versioning-policy).

## :beers: Contributing

Welcome contributing!

Please use GitHub's Issues/PRs.

See [CONTRIBUTING.md](CONTRIBUTING.md).

### Development Tools

- `npm test` runs tests and measures coverage.
- `npm run update` runs in order to update readme and recommended configuration.
- `npm run new [new rule name]` runs to create the files needed for the new rule.
- `npm run docs:watch` starts the website locally.

<!--DOCS_IGNORE_END-->

## :lock: License

See the [LICENSE](LICENSE) file for license rights and limitations (MIT).
