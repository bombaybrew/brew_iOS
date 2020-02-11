---
title: "Getting Started"
date: 2020-02-08
---

# Getting Started
---
Status: WIP

## What do i need to start building an iOS app?

1. Apple Mac computer.
2. An [IDE (Integrated development environment)](https://en.wikipedia.org/wiki/Integrated_development_environment) to write and compile our app. Apple [Xcode](https://developer.apple.com/xcode/) in this case.
3. Understanding of [Human Interface Guidelines.](https://developer.apple.com/design/human-interface-guidelines/)
4. Fluency with [Swift](https://developer.apple.com/swift/) programming language.
5. Source control system, for tracking changes to our source code. [Git](https://en.wikipedia.org/wiki/Git) in our case.

At very minimal our aproach to app development looks like this
![image caption here for xcode](/images/app_process.jpeg)

## Xcode 
  Xcode is an IDE(Integrated development environment) for Mac OS containing a suite of software development tools developed by Apple for developing softwares for iOS, iPadOS, watchOS etc. Xcode is a complete package that performs nearly all of the tasks that you need to do during software development such as :
1. Editor to write your code
2. Simulator to test your code across all the devices
3. Debugger to debug your code/User interface/memory allocation/CPU utilisation etc
4. Source control
5. Xcode server for Continuous Integration 
6. Create archives and deploy the app on App Store or export for Enterprise distribution  and many more……

For now, we will use it just for writing our code and run it on a simulator:) Refer below link to install Xcode in your Mac : 
https://developer.apple.com/support/xcode/ 


## Mac/Virtual Machine
   Xcode only runs on  Mac OS (Apple’s strategy to promote their platform :P). So, you need a Mac OS. If you have a MacBook , Great ! If not, there are some workarounds such as using virtual machine but that need some expertise in setting up those environment. Also, it’s more likely that you may face some issues such as slow performance while using Xcode through these virtual machines. You can refer below for more information:
https://codewithchris.com/xcode-for-windows/

## Swift/Objective C
   Once you are done with installing Xcode, let’s come to the favourite question of developers - Which programming language is used for developing IOS apps ? Well, we are focusing strictly to native apps here. So, there are two choices :
   1. Objective C

      Objective C was the primary language for app development till 2014 I.e. introduction of Swift. Objective C is a superset of C language with added object oriented capabilities. Objective C is being 30 years old now and does not support modern programming language needs. So, here is the solution from Apple, Swift

   2. Swift
   
      Swift was introduced by Apple in 2014 and provides modern language features such as dynamic, safe, late binding, and extensibility.  Earlier in 2018, Swift surpassed Objective-C in popularity and became the #1 programming language for iOS and other Apple operating systems. Swift is a highly recommended language for building your new iOS, tvOS, and watchOS platforms.

   C and C++ : You can still use C and C++ wherever required. During most of your coding, you would not need to use C and C++. It’s required only in certain situations where you need to interact with device hardware using low level APIs for which high level objective C/Swift abstraction is not available.


