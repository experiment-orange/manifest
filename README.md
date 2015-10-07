This is a general purpose skeleton manifest for a cross-dev development environment with minimal packages. The
manifest configures [git-repo](https://code.google.com/p/git-repo/) tool to synchronize a set of GIT repositories.

## What is included

* [JuNEST](http://fsquillace.github.io/junest-site/documentation.html) tools for a jailed
[ArchLinux](https://www.archlinux.org/) setup
* [unionfs-fuse](https://github.com/rpodgorny/unionfs-fuse) checked out to a stable release
* The latest and greatest stable [fuse](http://sourceforge.net/p/fuse/fuse/ci/master/tree/)
* Facade script and its libraries

These component are necessary to realize the development environment function.

## Configuration management

Users are encouraged to fork this repository and add their own manifests. The default manifest name sought by `repo`
is `default.xml`. This basic manifest is named `skeleton.xml`, so fork maintainers can have `default.xml` for
themselves.

According to the [documentation](https://gerrit.googlesource.com/git-repo/+/master/docs/manifest-format.txt), a
`skeleton.xml` may be included to another manifest as follows:

```xml
<include name="skeleton.xml"/>
```

The fork should be regularly merged with the upstream for updates.

## Branching policy

* `master` - is a stable branch
* `next` - is a development branch

Stable receives frozen manifests, but does not update often. Development is more relaxed w.r.t. component revisions
and the content may update frequently. However, there is less merging perceived.

You choose for yourself what do you base your work off. There is always a trade-off.
