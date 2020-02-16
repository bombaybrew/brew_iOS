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

1. Launch Xcode and click on "Create a new xcode project"
2. Xcode will ask you to choose a template. When we select a template, Xcode generates the boilderplate code required for that template. For now, let's select "Single View App".

   ![image caption here for xcode](/images/Xcode_ChooseTemplate.png)

3. Assign a product name i.e. Name of the product/app you want to build. In our case, let's call it "Ok Computer".
4. Put your organisation name if you wish to. Otherwise put any dummy name such as "mycompany". We will use Bombay Brew.
5. Organisation identifier - This is a mandatory field and the next field "Bundle Identifier" is derived from this one. Bundle identifier is an unique key that is assigned to your app.
6. Select "Swift" for language and leave other three boxes unchecked and click on "Next".

   ![image caption here for xcode](/images/Xcode_ProductName.png)

7. If you notice left pane of your Xcode, you can see some pregenerated files. This is the boilerplate code Xcode has generated for you depending upon the template you have chosen in step 2

   ![image caption here for xcode](/images/Xcode_TemplateFiles.png)

8. Let's build and run our app and see what happens. You can find "Build" and "Run" options in "Product" menu. You can use also use shortcuts "Command + B" and "Command + R" respectively.

   ![image caption here for xcode](/images/Simulator_InitialProduct.png)

9. When we run our app, Xcode builds the project first and if there are no errors, it will launch our app in a Simulator which shows a blank screen. As the name suggests, simulator is simulation of a physical device (iphone/ipad/Apple watch etc) that allows you to visualise your app without the need of physical device. Although, you can work with simulator most of the time, it's recommended that you test your app on a device before shipping to production as there are some features such as Face Id/Touch Id that can not be tested on a simulator ( at least as of now. Xcode may introduce this feature in future). Sometimes, there might be different behaviour of the same code when it is run on a simulator than when run on a device.
   Time to code now :)
10. Select Main.storyboard file which can be found on the left pane of Xcode. You can see one View Controller similar to what we just saw in Simulator - a blank white screen. This .storyoard file will help you create your user interface of the app. You can even create user interface programatically but for now, let's use storyboard.
11. Select Library button as shown in the below image. This library is a list of all the UI components such as labels, buttons,text fields etc. you need to build your app. These are system UI components provided by Apple. You can create your own UI components as per the requirement.

   ![image caption here for xcode](/images/Xcode_UILibrary.png)

12. Search for "UILabel" in this library and drag drop on View Controller wherever we want the label to be placed. Double click to change the default label from "Label" to "Ok Computer".
13. That's it. Your "Ok Computer" app is ready. Hit "Command + R" and see your app in simulator.

   ![image caption here for xcode](/images/Simulator_FinalProduct.png)
