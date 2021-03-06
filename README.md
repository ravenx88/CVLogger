# CVLogger

[![CI Status](http://img.shields.io/travis/cvillaseca/CVLogger.svg?style=flat)](https://travis-ci.org/cvillaseca/CVLogger)
[![Version](https://img.shields.io/cocoapods/v/CVLogger.svg?style=flat)](http://cocoapods.org/pods/CVLogger)
[![License](https://img.shields.io/cocoapods/l/CVLogger.svg?style=flat)](http://cocoapods.org/pods/CVLogger)
[![Platform](https://img.shields.io/cocoapods/p/CVLogger.svg?style=flat)](http://cocoapods.org/pods/CVLogger)

`CVLogger` is a tool that shows a button over UIWindow (only DEBUG build). When it pushed will show any log printed by NSLog. 

![screenshot](https://cloud.githubusercontent.com/assets/7700085/13968554/b0c61910-f07d-11e5-9ced-33dadfe06c4a.gif)

[Show Appetize.io DEMO](https://appetize.io/app/kuz81bjqm91ucwzmtgeqpk55kc?device=iphone5s&scale=75&orientation=portrait&osVersion=9.2)

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

In your AppDelegate.h:
```objective-c
#import <CVLogger/CVLogger.h>

@property (strong, nonatomic) CVLogger *cvlogger;
```

In your AppDelegate.m:
```objective-c
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
//UIWindow must not be nil before init CVLogger
#ifdef DEBUG
    self.cvlogger =[[CVLogger alloc] init];
#endif
}
```

## Requirements

`CVLogger` works on iOS 7+ and requires ARC to build. It depends on the following Apple frameworks, which should already be included with most Xcode templates:

* Foundation.framework
* UIKit.framework

You will need the latest developer tools in order to build `CVLogger`. Old Xcode versions might work, but compatibility will not be explicitly maintained.

## Installation

CVLogger is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "CVLogger"
```

## Author

Cristian Villaseca, cvillaseca_basco@hotmail.com

## License

CVLogger is available under the MIT license. See the LICENSE file for more info.
