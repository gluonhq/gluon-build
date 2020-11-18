# gluon-build

This action builds a Gluon app using maven for a specific target platform. 
TODO: add link to example

Optionally it also sets the Gluon license before building.

* You need a Gluon project with a Maven build
* You need to setup GraalVM in your workflow
* For certain target platforms extra steps might be needed in your workflow (e.g. setup Apple certificates for iOS)

# Usage

```yaml
steps:
- uses: actions/checkout@latest
- uses: DeLaGuardo/setup-graalvm@master
  with:
    graalvm-version: '20.3.0.java11' 
- name: Gluon Build
    uses: gluonhq/gluon-build@v1
    with:
      gluon-license: ${{ secrets.GLUON_LICENSE }}
      target: 'ios'
```

# License

The project is licensed under GPL 3. See LICENSE file for the full license.

