# Swift Express

[![GitHub license](https://img.shields.io/badge/license-LGPL v3-lightgrey.svg)](https://raw.githubusercontent.com/crossroadlabs/Express/master/LICENSE)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
![Platform OS X | Linux](https://img.shields.io/badge/platform-OS%20X%20%7C%20Linux-orange.svg)

### Swift Express is a simple, yet unopinionated web application server written in Swift

## Getting started

##### Create a project:

```sh
swift-express init HelloExpress
cd HelloExpress
open HelloExpress.xcodeproj
```

##### Create new API:

```swift
app.get("/myecho") { request in
    return Action<AnyContent>.ok(AnyContent(str: request.query["message"]?.first))
}
```

##### Run from xCode or command line with:

```sh
swift-express run
```

Test it in the browser: [http://localhost:9999/myecho?message=Hello](http://localhost:9999/myecho?message=Hello)


## Installation

[//]: # (Icons are here: https://www.iconfinder.com/icons/395228/linux_tox_icon#size=16)

### [OS X ![OS X](https://cdn1.iconfinder.com/data/icons/system-shade-circles/512/mac_os_X-16.png)](http://www.apple.com/osx/)

##### First install the following components (if you have not yet):

* [XCode](https://developer.apple.com/xcode/download/) 7.2 or higher
* [Homebrew](http://brew.sh/) the latest available version
* Command Line tools: run ```xcode-select --install``` in terminal

##### Run the following in terminal:

```sh
brew tap crossroadlabs/tap
brew install swift-express
```

#### [Linux ![Linux](https://cdn1.iconfinder.com/data/icons/system-shade-circles/512/linux_tox-16.png)](http://www.linux.org/)

##### Stay tuned! We are working hard on this.

## Examples

### Hello Express:

Create a project as it is described in the getting started section and add the following lines before server start:

```swift
app.get("/hello") { request in
    return Action<AnyContent>.ok(AnyContent(str: "<h1>Hello Express!!!</h1>", contentType: "text/html"))
}
```

Launch the app and follow the link: [http://localhost:9999/myecho?message=Hello](http://localhost:9999/myecho?message=Hello)

## Ideology behind

### Taking the best of swift

[Swift](https://swift.org/) essentially is a new generation programming language combining simplicity and all the modern stuff like functional programming.

We were inspired (and thus influenced) mainly by two modern web frameworks: [Express.js](http://expressjs.com/) and [Play](https://www.playframework.com/). So, we are trying to combine the best of both worlds taking simplicity from [Express.js](http://expressjs.com/) and modern robust approach of [Play](https://www.playframework.com/)

Let us know if we are on the right path! Influence the project, create feature requests, API change requests and so on. While we are in our early stages, it's easy to change. We are open to suggestions!

## Roadmap

* v0.2: advanced paths and regex url matching support
* v0.3: Linux support
* v0.4: proper streaming APIs
* v0.5: more content types available out of the box
* v0.6: Web Sockets
* v1.0: hit the production!

## Changelog

* v0.1: Initial Public Release
	* basic routing
	* views and view engines (supports Mustache)
	* JSON rendering as a view
	* query parsing
	* static files serving

## Contributing

To get started, <a href="https://www.clahub.com/agreements/crossroadlabs/Express">sign the Contributor License Agreement</a>.

## [![Crossroad Labs](http://i.imgur.com/iRlxgOL.png?1) by Crossroad Labs](http://www.crossroadlabs.xyz/)
