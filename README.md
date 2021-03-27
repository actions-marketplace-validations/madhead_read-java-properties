# madhead/read-java-properties

GitHub Action to read values from Java's `.properties` files.

## Usage

```yaml
- uses: madhead/read-java-properties@latest
  id: version
  with:
    file: gradle.properties
    property: version
    default: 0.0.1

- run: echo ${{ steps.version.outputs.value }} # Project's version from gradle.properties or 0.0.1 if it is not defined there
```

To see the list of available versions of this action (`latest` in the example above), navigate to the [Releases & Tags](https://github.com/madhead/read-java-properties/tags) page of this repo.
Whenever a new version is released, corresponding tags are created / updated.
`latest` tag always points to the latest release.
`master` label could also be used, being a synonym to `latest`.
There are also `$major` and `$major.$minor` tags pointing to the latest matching version (i.e. tag `1` always points to the latest `1.x` version, and tag `1.1` — to the latest `1.1.x` version).

To see this action… in action… check its integration test in [`test.yml`](.github/workflows/test.yml).
