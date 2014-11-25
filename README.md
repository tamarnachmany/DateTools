## DateTools: The Breakup
![Banner](http://www.addmyclassified.com/wp-content/uploads/2014/05/broken-heart.png)

DateTools: The Breakup is a fork of DateTools, which divides its powerhouse category (NSDate+DateTools) into several classes based on the single responsibility principle. These classes can be used to transform the way dates are presented on your app.

The original Date Tools has about 107 methods in its DateTools category. Because they are all grouped together, they are all imported into a class in one line of code. The Breakup divides these methods among several classes according to their purpose, making the codebase easier to understand and use.

The methods used by these classes have been taken directly from Date Tools, so all the functionalities of the original CocoaPod have been preserved. For information on what Date Tools can do, visit the [DateTime] (https://github.com/MatthewYork/DateTools).  

## Installation

**Cocoapods**

Add Code Pod Link

**Manual Installation**

All the classes required for DateTools are located in the DateTools folder in the root of this repository. They are listed below:


* <code>DTConstants.{h,m}</code>
* <code>DTError.{h,m}</code>
* <code>DTTimePeriod.{h,m}</code>
* <code>DTTimePeriodChain.{h,m}</code>
* <code>DTTimePeriodCollection.{h,m}</code>
* <code>DTTimePeriodGroup.{h,m}</code>
* <code>DateTools.h</code>
* <code>NSDate+Comparators.{h,m}</code>
* <code>NSDate+ComponentForDate.{h,m}</code>
* <code>NSDate+ComponentForDateWithoutCalendar.{h,m}</code>
* <code>NSDate+DateByAdding.{h,m}</code>
* <code>NSDate+DateBySubtracting.{h,m}</code>
* <code>NSDate+DateComponentsWithCalendar.{h,m}</code>
* <code>NSDate+DateTools.{h,m}</code>
* <code>NSDate+FormattedWithFormat.{h,m}</code>
* <code>NSDate+FormattedWithStyle.{h,m}</code>
* <code>NSDate+Helpers.{h,m}</code>
* <code>NSDate+LocalizedStrings.{h,m}</code>
* <code>NSDate+TimeAgo.{h,m}</code>
* <code>NSDate+TimeFrom.{h,m}</code>
* <code>NSDate+TimeFromCalendar.{h,m}</code>
* <code>NSDate+TimeFromCalendar.{h,m}</code>
* <code>NSDateConstants.{h,m}</code>


The following bundle is necessary if you would like to support internationalization:

* <code>DateTools.bundle</code>


## Usage

Date Tools gives you access to many different methods that modify the way NSDate objects are presented on iOS apps 

For a full documentation, please refer to the Date Tools ReadMe.

The primary difference between these two CocoaPods is that The Breakup changes NSDate+DateTools (one category on NSDate with many different types of methods, divided by #pragma mark) into several NSDate categories. Categories add methods to existing classes. 

In this version, the comparator methods are all in one category, because these are all used for more or less the same purpose. In general, though, I have erred on the side of dividing methods as much as possible based on their purposes. For instance, dateByAdding and dateBySubtracting methods are in two separate categories.

Like Date Tools, NSDateTools: The Breakup offers a handful of methods that change the way dates can be displayed on your apps:

####NSDate+TimeAgo 

This CocoaPod’s Time Ago methods (now found in NSDate+TimeAgo) change the way dates are displayed on your app. 

####NSDate+LocalizedStrings

Using this category, you can easily translate the dates on your app into 32 languages (with two Chinese dialects). 	

####NSDate+DateComponentsWithCalendar

This category streamlines the process 		of getting date components from an NSDate. 

Without Date Tools, you have to create a whole bunch of objects to get date components from an NSDate:

```objc
1. Create calendar
NSCalendar *calendar = [[NSCalendar alloc] initWithCalendarIdentifier:NSGregorianCalendar];
unitFlags = NSCalendarUnitHour | NSCalendarUnitMinute | NSCalendarUnitSecond;

NSDateComponents *dateComponents = [calendar components:unitFlags fromDate:date];

2. Get components
NSInteger hour = dateComponents.hour;
NSInteger minute = dateComponents.minute;
NSInteger second = dateComponents.second;

```

With DateTools, grabbing components from a date is as simple as:

```objc
NSInteger hour = date.hour;
NSInteger minute = date.minute;
NSInteger second = date.second;
```


Thanks to  Matthew York for his work on Date Tools, Kevin Lawler for his work on [NSDate+TimeAgo](https://github.com/kevinlawler/NSDate-TimeAgo), and all the others who have contributed to this CocoaPod. 


