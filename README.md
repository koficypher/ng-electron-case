[![Known Vulnerabilities](https://snyk.io/test/github/koficypher/ng-electron-case/badge.svg?targetFile=package.json)](https://snyk.io/test/github/koficypher/ng-electron-case?targetFile=package.json)

# NgElectronCase

Electron boilerplate with Angular 7 on the frontend for building desktop applications. It comes with an angular module [NGxElectron](https://github.com/ThorstenHans/ngx-electron) which is an angular wrapper for interacting with electron's renderer API.

## Features

- Electron's renderer process available as a service in Angular. See [NGxElectron](https://github.com/ThorstenHans/ngx-electron) for in-depth documentation and examples.
- Electron packager for packaging your finished electron apps. See [Electron-Packager](https://github.com/electron-userland/electron-packager) for getting started and [here](https://github.com/electron-userland/electron-packager/blob/master/docs/api.md) for a deep-dive into their API.
- Electron Windows Installer for building out installers for windows systems. Also see [Electron-Windows-Installer](https://github.com/electron-userland/electron-installer-windows) for details.


## Typical WorkFlow
- Assuming you have finished building your application, you will first use the Electron packager to package your app into a folder like this:
  > `electron-packager <sourcedir> <appname> --platform=<platform> --arch=<arch> --out <outputdir>/`
- It will create the packaged app in the specified `<outputdir>` and you can inspect it to see for yourself
- After that you will then use the Electron Windows Installer which is the only supported installer as at now to convert your packaged app into a .exe and .msi per the documentation [here](https://github.com/electron-userland/electron-installer-windows) . E.g :
  > `electron-installer-windows --src packages/<folder-name>/ --config config.json`
- The above command has a `--config` flag which points to `config.json` file. Create that file in your app directory as it is what the module will look into for configuration options in building your installer.

> - Note the ff
> - Your app name should be consistent i.e. same name in your package.json and same name in all your configurations
> - Your package.json file should contain Author object with name, email and url, Name of app and Version as they are mandatory.



## Installation

Download this repo or git clone this repo with `git clone https://github.com/koficypher/ng-electron-case.git` and run
this command `npm install` to install all the dependencies for the project.

Documentation on how to use NGxElectron can be found [here](https://github.com/ThorstenHans/ngx-electron).

## Usage

Run `npm run electron` to start up the application.

## Using Native Modules

This application also comes with Electron Rebuild which rebuilds native Node.js modules against the currently installed Electron version. To use the rebuild feature edit the `package.json` file, in the scripts section where we have the rebuild command with the name of the module you want to rebuild. Further documentation can be found [here](https://github.com/electron/electron-rebuild)

## Tip To Reduce Build Size

Electron packager will use only your dependencies specified in your `package.json` file and also dependcies of those dependencies when packaging your app. I think you are getting the picture. That means you can actually reduce the size of the packaged app if you remove all unecessary packages to the devdepencies section in your `package.json` file. Additional `--prune=true` and using asar builds `--asar` will also add in reducing your build size. But in all, a zipped, minimal Electron application is approximately the same size as the zipped prebuilt binary for a given target platform, target arch, and Electron version.

## Licence

This project is licenced under MIT licence

## Bugs and Security Issues ??

Kindly email your findings to [me](mailto:skcypher6@gmail.com)

## Want To Collaborate ??

Kindly email [me](mailto:skcypher6@gmail.com)



