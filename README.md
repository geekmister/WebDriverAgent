# WebDriverAgent [![GitHub license](https://img.shields.io/badge/license-BSD-lightgrey.svg)](LICENSE) [![Build Status](https://travis-ci.org/facebook/WebDriverAgent.svg?branch=master)](https://travis-ci.org/facebook/WebDriverAgent) [![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)

WebDriverAgent is a [WebDriver server](https://w3c.github.io/webdriver/webdriver-spec.html) implementation for iOS that can be used to remote control iOS devices. It allows you to launch & kill applications, tap & scroll views or confirm view presence on a screen. This makes it a perfect tool for application end-to-end testing or general purpose device automation. It works by linking `XCTest.framework` and calling Apple's API to execute commands directly on a device. WebDriverAgent is developed and used at Facebook for end-to-end testing and is successfully adopted by [Appium](http://appium.io).

WebDriverAgent是一个在iOS设备或者虚拟机上实现了一个基于WebDriver协议的服务，这个服务可以远程控制iOS设备。你也可以启动且者杀死某些应用，点击且滚动视图或者确认某块视图是否出现在了屏幕中。这使它在应用端到端的测试和通用设备自动化中成为了一款完美的工具。它通过链接'XCTest.framework'和调用Apple's API来直接在设备上执行命令。WebDriverAgent在Facebook的端到端测试中被开发和使用，并被Appium成功采用。

## Archiving

We are archiving WebDriverAgent. Thanks to the community who have used it! The code will remain here for your future use, but will no longer be actively supported by Facebook.

我们正在存档WebDriverAgent。感谢社区的伙伴使用它！当你想使用时可以在这里找到代码，但是Facebook已不在提供积极的支持。

In May 2019, we open sourced IDB, “iOS Development Bridge”, a command line interface for automating iOS Simulators and Devices. We are currently migrating our own internal projects from WDA to IDB, and suggest checking it out as an alternative. 

2019年5月，我们开源了IDB，"iOS 开发桥梁"，一款用来自动化iOS模拟器和真机的命令行接口。我们当前正在迁移我们自己的内部项目从WDA过渡到IDB，并且建议你把IDB作为另外一个选择。（译者说：最后这句话翻译的不太好，我自己也使用过IDB，但是IDB在iOS真机上的操作和功能要比WDA受限，且IDB不支持跨平台，因为它依赖Mac操作系统）。

More information on IDB:
 * [Project on GitHub](https://github.com/facebook/idb/)
 * [Talk from 2019 F8](https://developers.facebook.com/videos/2019/reliable-code-at-scale/)

## Overview

WebDriverAgent is a [WebDriver server](https://w3c.github.io/webdriver/webdriver-spec.html) implementation for iOS that can be used to remote control iOS devices. It allows you to launch & kill applications, tap & scroll views or confirm view presence on a screen. This makes it a perfect tool for application end-to-end testing or general purpose device automation. It works by linking `XCTest.framework` and calling Apple's API to execute commands directly on a device. WebDriverAgent was developed and used at Facebook for end-to-end testing and is successfully adopted by [Appium](http://appium.io).

WebDriverAgent是一个在iOS设备或者虚拟机上实现了一个基于WebDriver协议的服务，这个服务可以远程控制iOS设备。你也可以启动且者杀死某些应用，点击且滚动视图或者确认某块视图是否出现在了屏幕中。这使它在应用端到端的测试和通用设备自动化中成为了一款完美的工具。它通过链接'XCTest.framework'和调用Apple's API来直接在设备上执行命令。WebDriverAgent在Facebook的端到端测试中被开发和使用，并被Appium成功采用。

## Features
 * Works with device & simulator
 * Implements most of [WebDriver Spec](https://w3c.github.io/webdriver/webdriver-spec.html)
 * Implements part of [Mobile JSON Wire Protocol Spec](https://github.com/SeleniumHQ/mobile-spec/blob/master/spec-draft.md)
 * [USB support](https://github.com/facebook/WebDriverAgent/wiki/USB-support) for devices
 * Inspector [endpoint](http://localhost:8100/inspector) with friendly user interface to inspect current device state
 * Easy development cycle as it can be launched & debugged directly via Xcode
 * Unsupported yet, but works with tvOS & OSX

## 特点
  * 可以在iOS真机和模拟器上工作
  * 实现大部分的WebDriver规范
  * 实现了部分Mobile JSON Wire Protocol规范
  * iOS真机支持USB
  * Inspector可以显示当前iOS真机或者模拟器的视窗，这点非常友好（译者说：关于这点大家还是忽略掉吧，我到现在都没有找到这个功能，因为在Facebook停止维护后，这个功能又在Appium的fork版本被去掉，很多版本都没有这个功能了）
  * 开发周期非常容易，因为它可以直接通过Xcode启动且调试
  * 当前不支持tvOS和OSX，但是可以跟它们合作

[![Demo Video](https://j.gifs.com/gJymG9.gif)](https://youtu.be/EatiYGFxBxY)

## Getting Started
To get the project set up just run bootstrap script:
```
./Scripts/bootstrap.sh
```
It will:
* fetch all dependencies with [Carthage](https://github.com/Carthage/Carthage)
* build Inspector bundle using [npm](https://www.npmjs.com)

After it is finished you can simply open `WebDriverAgent.xcodeproj` and start `WebDriverAgentRunner` test
and start sending [requests](https://github.com/facebook/WebDriverAgent/wiki/Queries).

More about how to start WebDriverAgent [here](https://github.com/facebook/WebDriverAgent/wiki/Starting-WebDriverAgent).

## Known Issues
If you are having some issues please checkout [wiki](https://github.com/facebook/WebDriverAgent/wiki/Common-Issues) first.

## For Contributors
If you want to help us out, you are more than welcome to. However please make sure you have followed the guidelines in [CONTRIBUTING](CONTRIBUTING.md).

## License

[`WebDriverAgent` is BSD-licensed](LICENSE). We also provide an additional [patent grant](PATENTS).

Have fun!
