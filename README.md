# Loki font loading issue reproduction

To reproduce the issue I set up a simpler version of the repo I am work with that has a Button and Header component which require a font that is loaded using an @font-face call done inside the Storybook preview configuration.

Notice that if running `loki test` against the local storybook the tests pass with the expected font styling. But if I build the static storybook and run `loki test --reactUri file:./storybook-static` the tests fail with the following message:

```bash
2 requests failed to load; file:///fonts/Inter-Regular.woff2, file:///fonts/Inter-Regular.woff
```
