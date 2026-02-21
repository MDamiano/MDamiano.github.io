# AGENTS

Project-specific guidance for coding agents working in this repository.

## Scope
- This file applies to the entire repository.

## Build & Run
- Install dependencies: `bundle install`
- Local dev server: `bundle exec jekyll serve --config _config.yml,_config-dev.yml`
- Build site: `bundle exec jekyll build`

## Conventions
- Keep edits minimal and focused.
- Preserve existing site style unless requested otherwise.
- Prefer small, reviewable commits.

## Validation
- Run `bundle exec jekyll build` after content or template changes.
- Check generated output in `_site/` when layout or styling changes.
- If fails occurs, show it loudly with clear error logs over failing silently with hidden fallbacks.
- when a unit test fails, first ask yourself: is this exposing a real bug in the production code — or is the test itself flawed?
