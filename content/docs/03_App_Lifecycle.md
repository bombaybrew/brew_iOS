---
title: "App Lifecycle"
date: 2020-02-16
---

# App Lifecycle
---
Status: WIP

## Differect states of an app through its entire lifecycle 

As humans or animals go through different phases in their lifetime so does an app. App goes through different states since the time you install it till it is uninstalled from the system. Knowing these states is important as system (iOS) imposes some restrictions as to what your app can do and what can not depending upon which state of the lifecycle the app is in at that moment. Let's explore these different states.
1. Not running 
2. Active
3. In Active
4. Background
5. Suspended

At any moment, your app belongs to one of these states.

## Not running 
   The app has not been launched or was running/suspended(more on suspended state later) and killed by system (on its own) or by user (manually).

## Active
   App is in foreground, running and is recieving UI events. 

## In Active 
   App is in foreground, running but is not recieving any UI events(It can execute some other code though) . This can happen when there are some high priority interrupts from the system such as a call or a message or a battery low alert.

## Background
   App is in background and executing some code.

## Suspended
   App is in background but is not executing any code. In this state, the app is loaded in memory but does not execute any code. If the app is launched from this suspended state, it will maintain the  same state when it was taken to background last time. In low memory situation, system will purge the apps in suspended state. In such a case, app does not get any callback

## App state transitions and their mapping to AppDelegate methods:
   
   Whenever there is a change in App State, your app delegate object gets callback to respond to those app state changes. Let's understand with examples the different app states transitions and the app delegate callback methods :

   1. Scenario : Let's suppose you just downloaded the app from App Store or you have killed it from app switcher. 
      App State : At this moment, the app is in Not running state. 

   2. Scenario : You launched the app by tapping on app icon
      App State: Not running -> In Active -> Active
      
      App Delegate callbacks:   
      1.func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool 

      2.func applicationDidBecomeActive(_ application: UIApplication)


   3. Scenario : You pressd Home button.

      App State: There are two cases here: 
      1. App is not configured to run in background : iOS allows approximately 5 sec to run the app in background although you can request more time from the system to run in background. After these 5 sec or reuested time gets over, iOS moves your app to Suspended state. Active -> Background -> Suspended
      2. App is configured to run in background e.g. Music Player : Such apps can keep runnning in background. Active -> Background

      App delegate callbacks: 

      1.func applicationWillResignActive(_ application: UIApplication)

      2.func applicationDidEnterBackground(_ application: UIApplication) 

   4. Scenario : After above scenario, you launch the app from App Switcher or tapping app icon. There two possible cases here :
      1. The app is in suspended state

         App State : Suspended -> Background -> Inactive -> Active
         App Delegate callbacks : 
         1. func applicationWillEnterForeground(_ application: UIApplication)
         2. func applicationDidBecomeActive(_ application: UIApplication)

      2. App got killed by OS - As mentioned above, a suspended state app may get purged by OS in low memory situation.

         App State : Not running -> Inactive -> Active

         App Delegate callbacks : 
      	 1.func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool 

      	 2.func applicationDidBecomeActive(_ application: UIApplication)

   5. Scenario: App is in foregrund and you kill the app

      App state : foreground -> background -> not running

      App Delegate callbacks : 
      1. func applicationWillResignActive(_ application: UIApplication)

      2. func applicationDidEnterBackground(_ application: UIApplication)

      3. func applicationWillTerminate(_ application: UIApplication)

   6. Scenario: App is in background (not suspended) and you kill the app

      App State: Background -> Not running

      App Delegate callbacks: func applicationWillTerminate(_ application: UIApplication)

   7. Scenario: App is in Suspended state and you kill the app(or system kills the app)

      App State : Suspended -> Not running

      Note: You don't get any callback if the app is killed from a Suspended State
 





