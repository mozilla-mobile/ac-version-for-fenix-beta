# ac-version-for-fenix-beta

This _GitHub Action_ determines the Android Components release that is used in the current Fenix Beta.

It publishes the major A-C release number in the `major-ac-version` output, which can then be used in other _GitHub Actions_.

Example usage:

```
      - name: "Discover A-C Version"
        id: ac-version-for-fenix-beta
        uses: mozilla-mobile/ac-version-for-fenix-beta@1.0.0
          
      - name "Print the version number"
        run: "The current A-C Release used in Fenix Beta is $${{steps.ac-version-for-fenix-beta.outputs.major-ac-version}}"
```

This _GitHub Action_ is used in in the [github.com/mozilla-mobile/android-components/blob/master/.github/workflows/sync-strings.yml](https://github.com/mozilla-mobile/android-components/blob/master/.github/workflows/sync-strings.yml) workflow.
