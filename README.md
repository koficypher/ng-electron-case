[![Known Vulnerabilities](https://snyk.io/test/github/koficypher/ng-electron-case/badge.svg?targetFile=package.json)](https://snyk.io/test/github/koficypher/ng-electron-case?targetFile=package.json)

# NgElectronCase

Electron boilerplate with Angular 7 on the frontend for building desktop applications. It comes with an angular module [NGxElectron](https://github.com/ThorstenHans/ngx-electron) which is an angular wrapper for interacting with electron's renderer API.

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.1.

## Installation

Download this repo or git clone this repo with `git clone https://github.com/koficypher/ng-electron-case.git` and run
this command `npm install` to install all the dependencies for the project.

Documentation on how to use NGxElectron can be found [here](https://github.com/ThorstenHans/ngx-electron).

## Usage

Run `npm run electron` to start up the application.

## Using Native Modules

This application also comes with Electron Rebuild which rebuilds native Node.js modules against the currently installed Electron version. To use the rebuild feature edit the `package.json` file, in the scripts section where we have the rebuild command with the name of the module you want to rebuild. Further documentation can be found [here](https://github.com/electron/electron-rebuild)

## Future Feature Updates

- Support for building Installers
- Many more to come 

