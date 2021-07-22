﻿tdlib.native Maintainership
===========================

Publish a New Version
---------------------

1. Update the Git submodule containing the sources, make sure everything builds correctly
2. Update the license, if required.
3. Push a version tag (`v1.x.x`) to this repository. CI servers will do their job and upload the artifacts to the [Releases][releases] page.
4. Pack and upload the NuGet, as described below.

How to pack to NuGet
--------------------

Pack script requires NuGet 5 to be installed on a machine.

```console
$ pwsh ./common/download-release.ps1
$ pwsh ./common/nuget-pack.ps1
```

Then upload the `build/tdlib.native.<VERSION>.nupkg` to the NuGet server.

[releases]: https://github.com/ForNeVeR/tdlib.native/releases