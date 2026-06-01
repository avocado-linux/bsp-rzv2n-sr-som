# bsp-rzv2n-sr-som

Board support for the SolidRun RZ/V2N SoM on HummingBoard IIOT

## Using this extension

`bsp-rzv2n-sr-som` is an [Avocado](https://avocadolinux.org) extension — a reusable fragment of
build- and runtime-configuration that you compose into your own Avocado project. To use it,
declare it as a package-sourced extension in your `avocado.yaml` and add it to a runtime:

```yaml
extensions:
  avocado-bsp-rzv2n-sr-som:
    source:
      type: package
      version: "*"        # or pin an exact version

runtimes:
  my-runtime:
    extensions:
      - avocado-bsp-rzv2n-sr-som
```

Then `avocado build`. The extension's config is fetched from your target's package feed
and merged into your project at build time.
