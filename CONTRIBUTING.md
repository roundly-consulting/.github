# Contributing

Thanks for helping improve the open-source packages of
[Roundly Consulting](https://roundly-consulting.com). Issues and pull requests are welcome.

This guide applies to every repository in the organisation that does not ship its own
`CONTRIBUTING.md`. By taking part you agree to follow our [Code of Conduct](https://github.com/roundly-consulting/.github/blob/main/CODE_OF_CONDUCT.md).

## Reporting bugs and requesting features

- **Bugs:** open an issue with the package version, your PHP and Laravel versions, the steps to
  reproduce, and what you expected to happen.
- **Features:** open an issue describing the use case first. For larger changes, please wait for
  a maintainer to agree on the approach before you write the code — it saves both of us time.
- **Security issues:** never open a public issue — follow the [security policy](https://github.com/roundly-consulting/.github/blob/main/SECURITY.md).

## Development setup

Our Laravel packages (`*-for-laravel`) need PHP 8.4 and Composer.

```bash
git clone https://github.com/roundly-consulting/<package>.git
cd <package>
composer install
```

Every package has the same scripts:

| Command | What it does |
|---|---|
| `composer test` | Runs the Pest test suite |
| `composer test-coverage` | Runs the tests with a coverage minimum |
| `composer format` | Formats the code with Laravel Pint |
| `composer analyse` | Runs Larastan (PHPStan) at level 7 |

## Pull request checklist

- [ ] Every change is covered by tests. A bug fix starts with a test that fails without the fix.
- [ ] `composer format`, `composer test`, `composer test-coverage` and `composer analyse` pass.
      The coverage minimum is the `--min` value in the package's `.github/workflows/run-tests.yml`.
- [ ] Public behaviour changes are documented in the package's `README.md`.
- [ ] No new runtime dependency outside the policy below.

## Dependency policy

A package's runtime dependencies (`require` in `composer.json`) may only be:

- PHP and its extensions (`php`, `ext-*`);
- official Laravel packages (`illuminate/*`, `laravel/*`);
- official Symfony components (`symfony/*`);
- other Roundly packages (`roundly-consulting/*-for-laravel`).

If a feature seems to need another runtime library, please open an issue first — we usually
implement it natively instead. Development dependencies (`require-dev`) are not restricted.

## Commits

We use [Conventional Commits](https://www.conventionalcommits.org) with a scope, for example
`fix(validation): reject empty ranges` or `feat(cast): add nullable money cast`. Signed commits
are appreciated. Both are optional for contributors: maintainers may rewrite commit messages when
merging a pull request.

## License

By contributing, you agree that your contributions are licensed under the license of the
repository you contribute to (MIT for our packages — see its `LICENSE.md`).
