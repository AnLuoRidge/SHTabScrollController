# SHTabScrollController

[![CI Status](http://img.shields.io/travis/@harushuu/SHTabScrollController.svg?style=flat)](https://travis-ci.org/@harushuu/SHTabScrollController)
[![Version](https://img.shields.io/cocoapods/v/SHTabScrollController.svg?style=flat)](http://cocoapods.org/pods/SHTabScrollController)
[![License](https://img.shields.io/cocoapods/l/SHTabScrollController.svg?style=flat)](http://cocoapods.org/pods/SHTabScrollController)
[![Platform](https://img.shields.io/cocoapods/p/SHTabScrollController.svg?style=flat)](http://cocoapods.org/pods/SHTabScrollController)

## Screenshots
![image](https://github.com/harushuu/SHTabScrollController/raw/master/Screenshots.gif)

## Installation
 
With [CocoaPods](http://cocoapods.org/), add this line to your `Podfile`.

```
pod 'SHTabScrollController', '~> 0.3.3'
```

and run `pod install`, then you're all done!

## How to use

```objc
NSArray *titles = @[@"tab0", @"tab1", @"tab2"];
NSArray *controllers = @[[[YourViewController alloc] init], 
                         [[YourViewController alloc] init], 
                         [[YourViewController alloc] init]];

// default init method, do not care about switch controllers, 
// will auto switch current controller when tap or scroll
SHTabScrollController *tabScrollController = [SHTabScrollController setupTitles:titles 
                                                                    controllers:controllers];
```

## Summary

A simple view controller with tab button and childViewController, inspired by Netease News.

Will add more custom option in next version.

Tab button had some animation and childViewController can be scroll.

Enjoy yourself!

###custom

```objc
// if you wanna to get current tab index, you should call this method
+ (SHTabScrollController *)setupTitles:(NSArray *)titles 
                           controllers:(NSArray *)controllers 
                        tabIndexHandle:(SHTabIndexHandle)tabIndexHandle;

// default is blackColor
@property (nonatomic, strong) UIColor *normalTitleColor;

// default is redColor
@property (nonatomic, strong) UIColor *selectedTitleColor;

// default is [UIColor colorWithRed:53.f/255.f green:53.f/255.f blue:53.f/255.f alpha:1.f], 
// which likes a kind of blackColor
@property (nonatomic, strong) UIColor *normalTabBottomLineColor;

// default is [UIColor colorWithRed:205.f/255.f green:67.f/255.f blue:67.f/255.f alpha:1.f], 
// which likes a kind of redColor
@property (nonatomic, strong) UIColor *selectedTabBottomLineColor;

// default is 40.0
@property (nonatomic, assign) CGFloat tabButtonHeight;

// default is nil (system font 17 plain)
@property (nonatomic, strong) UIFont *tabTitleFont;
```

## Requirements

* iOS 8.0+ 
* ARC

## Author

@harushuu, hunter4n@gmail.com

## License

English: SHTabScrollController is available under the MIT license, see the LICENSE file for more information.     

