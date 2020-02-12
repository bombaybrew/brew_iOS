---
title: "OK Computer"
date: 2020-02-08
---

# OK Computer
---
Status: WIP

## Building a Hello World app

A 'Hello World' program is a very effective way to learn a new language or programming concept.

As a tribute to one of my favourite music band [RadioHead](https://en.wikipedia.org/wiki/Radiohead), we are going to do a ['OK Computer'](https://en.wikipedia.org/wiki/OK_Computer) instead of 'Hello World'.

## Setup for Ok Computer

Let's start with creating our super simple iOS app - OK Computer. We are assuming that you are ready with the initial set up required as mentioned in "Getting Started" :

1. Launch Xcode and click on "Create a new xocde project"
2. Xcode will ask you to choose a template. When we select a template, Xcode generates the boilderplate code required for that template. For now, let's select "Single View App".
3. Assign a product name i.e. Name of the product/app you want to build. In our case, let's call it "Hello Computer".
4. Organisation name as MyCompany
5. Organisation identifier - This is a mandatory field and the next field "Bundle Identifier" is derived from this one. Bundle identifier is an unique key that is assigned to your app.
6. Select "Swift" for language and leave other three boxes unchecked.
7. Click on "Next"
8. If you notice left pane of your Xcode, you can see some pregenerated files. This is the boilerplate code Xcode has generated for you depending upon the template you have chosen in step 2
9. Let's build and run our app and see what happens. You can find "Build" and "Run" options in "Product" menu. You can use also use shortcuts "Command + B" and "Command + R" respectively.
10. When we run our app, Xcode builds the project first and if there are no errors, it will launch our app in a Simulator which shows a blank screen. As the name suggests, simulator is simulation of a physical device (iphone/ipad/Apple watch etc) that allows you to visualise your app without the need of physical device. Although, you can work with simulator most of the time, it's recommended that you test your app on a device before shipping to production as their are some features such as Face Id/Touch that can not be tested on a simulator or sometimes, there might be different behaviour of the same code when it is run on a simulator than when run on a devcie.
