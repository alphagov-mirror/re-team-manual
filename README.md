# Reliability Engineering Team Manual [![Build Status](https://travis-ci.org/alphagov/re-team-manual.svg?branch=master)](https://travis-ci.org/alphagov/re-team-manual)

## Technical documentation

This is a static site generated with Middleman.

## Tech docs template

This project uses [alphagov/tech-docs-template](https://github.com/alphagov/tech-docs-template).

### Dependencies

- Ruby.
- The `middleman` gem.

### Making changes

To make changes, edit the source files in the `source` directory. To add a
completely new page, create a file with a `.html.md` extension in the `/source`
directory.

Whilst writing documentation we can run a middleman server to preview how the
published version will look in the browser. After saving a change the preview in
the browser will automatically refresh. Run `bundle exec middleman server`,
then the website will be available locally at http://localhost:4567.

### Building the project

Build the site with:

        bundle exec middleman build

This will create a bunch of static files in `/build`.

### Deployment

This is deployed automatically to the PaaS via [the multi-tenant Concourse](https://cd.gds-reliability.engineering/teams/autom8/pipelines/internal-apps) via the [internal-apps pipeline in the tech-ops repo](https://github.com/alphagov/tech-ops/blob/master/reliability-engineering/pipelines/internal-apps.yml). (The Autom8 team is a good place to start with any questions).

## Licence

[MIT License](LICENCE.md)

## Pre-commit hooks

There are pre-commit hooks available to help when creating or editing markdown.

Install [pre-commit][] and the [vale][] linter:

```sh
brew install vale pre-commit
pre-commit install
```

The styles are copied from https://github.com/alphagov/govuk-developer-docs/tree/bc94d39dce23236fc61238464010713daf5213f9/styles

[pre-commit]: https://github.com/pre-commit/pre-commit
[vale]: https://errata-ai.github.io/vale/
