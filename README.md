# rk.downloadAppImage

This R package provides a GUI to install or update an AppImage of RKWard.

![rk.downloadAppImage main tab](./inst/screenshots/main_tab.png?raw=true "rk.downloadAppImage main tab")

It is a plugin package for [RKWard](https://rkward.kde.org), a powerful GUI and IDE for [R](https://r-project.org),
and will **only work in conjunction with RKWard**. However, RKWard is free software, please
[check it out](https://rkward.kde.org).

## Installation

### Installation via RKWard

After you installed RKWard, simply install this package like any other R package. The easiest way to get the most
recent stable release is to use RKWard's package management:

- Go to `Settings` -> `Manage R packages and plugins...` -> `Install/Update/Remove R packages`
- Check `Show only packages providing RKWard dialogs` and look at `New Packages`
- Check the desired package(s) and hit `Apply`

After you installed the package, RKWard should immediately have additional menu entries -- there's
usually no need to restart the application.

### Installation via GitHub

To install it directly from GitHub, you can use `install_github()` from the [devtools](https://github.com/r-lib/devtools) package:

```
devtools::install_github("rkward-community/rk.downloadAppImage") # stable release
devtools::install_github("rkward-community/rk.downloadAppImage", ref="develop") # development release
```

You can safely ignore warnings about the (unavailable) package "rkward", it was installed together with RKWard.

By the way, this is basically what the GUI implements.
 
## Contributing

See http://api.kde.org/doc/rkwardplugins/ for documentation on writing plugins for RKWard.
Please contact the [RKWard development mailing list](https://mail.kde.org/mailman/listinfo/rkward-devel)
for help, reports and requests.

- Submit pull requests or patches
- Contact us to get write access

This plugin is built using the [rkwarddev](https://files.kde.org/rkward/R/pckg/rkwarddev/index.html) package. This means that its development is mainly focussed on one
script file, located at `rk.downloadAppImage/inst/rkward/rkwarddev_rk.downloadAppImage_plugin_script.R`. This script is written in `R` code and *generates*
all of the other plugin files when run. Therefore, in case you'd like to add to this plugin, please add to this script file.

### Branches

Please note that all development happens in the `develop` branch. Pull requests against the `main` branch will be rejected, as it is reserved for the current stable release.

## Licence

Copyright 2024 Meik Michalke <meik.michalke@hhu.de>

rk.downloadAppImage is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

rk.downloadAppImage is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with rk.downloadAppImage.  If not, see <http://www.gnu.org/licenses/>.
