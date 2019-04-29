# CT General Cheet Sheet (V1)

This cheat sheet serves as a go-to guide of fancy and fun shortcuts that i have found as i continue to develop. 
I am tired of always having to search on google for Things I have done too many times before, but sporadic enough
for me to ever remember them.

*note: This also a fun jumping off point to force myself to learn Markdown and documentation in general. Hopefully it will make sense and be easy to follow. but don't expect it to.*

# Table of Contents
1. [Mobile Dev](#Mobile-Dev)

# Mobile Dev
From quick fixes to build problems, terminal requests to quickly run simulators. Anything and every little thing related in this space will be found here.

## Simulators

### Starting iOS Simulators W/out Xcode

- Command to see list of available devices
    ```sh
    xcrun simctl list
    ```
- if you are lucky, you will see something like this:
    ```sh
    ...
    == Runtimes ==
    iOS 12.1 (12.1 - 16B91) - com.apple.CoreSimulator.SimRuntime.iOS-12-1 
    tvOS 12.1 (12.1 - 16J602) - com.apple.CoreSimulator.SimRuntime.tvOS-12-1 
    watchOS 5.1 (5.1 - 16R591) - com.apple.CoreSimulator.SimRuntime.watchOS-5-1 
    == Devices ==
    -- iOS 12.1 --
        iPhone 5s (0F49A839-7DA8-49C0-A79F-91EF91B8CA74) (Shutdown) 
        iPhone 6 (53540384-0A01-48D4-AC99-41CB0ECF83A8) (Shutdown) 
        iPhone 6 Plus (91A9EA01-BB0B-454C-9D5A-3A86E8D37033) (Shutdown) 
        iPhone 6s (E2EB0968-92A0-4E45-8EA6-AE144B3BAE9B) (Shutdown) 
        iPhone 6s Plus (0796DCA4-0CBA-4315-8833-1F5BA793DEB6) (Shutdown) 
        iPhone 7 (6F1E791D-D254-44ED-AA23-9811F1FD42D3) (Shutdown)
    ...
    ```
- you can choose your device, and start a simulator by running the command below:
    ```sh
    /Applications/Xcode.app/Contents/Developer/Applications/Simulator.app/Contents/MacOS/Simulator -CurrentDeviceUDID <YOUR-DEVICE-ID>
    ```
- once the device has started, and you want to get fancy, you can install and launch your project using the following commands
    ```sh
    xcrun simctl install <YOUR-DEVICE-ID> <PATH-TO-APPLICATION-BUNDLE>
    xcrun simctl launch <YOUR-DEVICE-ID> <BUNDLE-ID-OF-APP-BUNDLE>
    ```