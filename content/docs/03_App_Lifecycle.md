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


## Not running 
   The app has not been launched or was running/suspended(more on suspended state later) and killed by system (on its own ) or by user (manually).

## Active
   App is in foreground and recieving events. 

## In Active 
   App is in foreground but is not recieving any events. This can happen when there are some high priority interrupts from the system such as a call or a message or a battery low alert. In this case, app stays in the foreground but you can not interact with the app.

## Background
   App is in background and executing some code.

## Suspended
   App is in background but is not executing any code. In this state, the app is loaded in memory but does not execute any code. If the app is launched from this suspended state, it will maintain the  same state when it was taken to background last time. In low memory situation, system will purge the apps in suspended state and app does not get any notification.

## App states and their mapping to AppDelegate methods :


