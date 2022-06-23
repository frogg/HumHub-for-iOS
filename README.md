# HumHub App for iOS (with Push Notifications!)
A simple Swift-framework to create an iOS app for HumHub instances with native push-notifications.
The main goal of this project was to drive participant activity through push notifications on iOS devices.

## Set up the HumHub iOS app
Required URLs to set up in `AppDelegate.swift`:

```swift
let baseUrl = "https://vereinsheim.d-64.org"

HumHub.loginPage = "\(baseUrl)/user/auth/login"
HumHub.mainDashboard = "\(baseUrl)/dashboard"
HumHub.pathsToOpenInInAppBrowser = ["d-64.org/positionen"]
HumHub.notificationsOverview = "\(baseUrl)/notification/overview"
HumHub.messagesOverview = "\(baseUrl)/mail/mail/index"
HumHub.newMessage = "\(baseUrl)//mail/mail/create?ajax=1"
HumHub.notificationSettings = "\(baseUrl)/notification/user"
```


## Push Notifications via FireBase
1. Create a new Firebase project for your HumHub instance.
2. Enable Firebase push notifications on HumHub and connect it with your Firebase credentials.
3. Add the Firebase `GoogleService-Info.plist` to the Xcode project.


## Example App
This open source project has been created for the D64 Vereinsheim app which can be [downloaded for free](https://apps.apple.com/de/app/d64-vereinsheim/id1502757383) from the iOS AppStore (D64 member login required).

## What about Android?
An Android app is not available.
However, Android supports Push Notifications in Progressive Web Apps.
