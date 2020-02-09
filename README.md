# Open Identity - iOS SDK

[![Travis][img-travis-master]][url-travis-master]
[![Coverage Status][img-coveralls-master]][url-coveralls-master]
[![Codacy Badge][img-codacy]][url-codacy]
[![Release][img-jitpack]][url-jitpack]
[![License][img-license]][url-bintray]

[![GithubWatch][img-github-watchers]][url-github-watchers]
[![GithubStars][img-github-stars]][url-github-stars]
[![GithubForks][img-github-forks]][url-github-forks]

## Minimal Requirements
* Xcode 9.0 or above
* CocoaPods 1.1.0 or higher
* MacOS 10.11.5 or higher
* iOS 10.0 or higher

## Installing the SDK:
1. Add the 'OpenIdentitySDK' dependency to your Podfile, for example:

    ```swift
    target <yourTarget> do
        use_frameworks!
	    pod 'OpenIdentitySDK'
    end
    ```  
1. From the terminal, run:  
    ```swift
    pod install --repo-update
    ```

## Initializing the SDK
1. Open your Xcode project and enable Keychain Sharing (Under project settings > Capabilities > Keychain sharing)
2. Under project setting > info > Url Types, Add $(PRODUCT_BUNDLE_IDENTIFIER) as a URL Scheme
3. Add the following import to your AppDelegate.swift file:
	```swift
	import OpenIdentitySDK
	```
4. Initialize the SDK by passing the `clientId` and `discoveryEndpointUrl` parameters to the initialize method. A common, though not mandatory, place to put the initialization code is in the application:didFinishLaunchingWithOptions: method of the AppDelegate in your Swift application.
    ```swift
    OpenIdentity.sharedInstance.initialize(clientId: <clientId>, discoveryEndpointUrl: <url>)
    ```

5. Add the following code to you AppDelegate file
    ```swift
    func application(_ application: UIApplication, open url: URL, options :[UIApplicationOpenURLOptionsKey : Any]) -> Bool {
        return OpenIdentity.sharedInstance.application(application, open: url, options: options)
    }
    ```

## Authenticating with service provided login UI
(aka authorization code grant)

## Authenticating with custom UI
(aka resource owner password credential grant)

## Authenticating with refresh token

## Logging out

## Invoking protected resources

### Access and Identity tokens

### Using access token to make requests to protected resources

## Self-service

### Sign up

### Change Password

### Forgot Password

### Update Profile

## Got Questions?
Join us on [Slack](https://public-slack-channel.com) and chat with our dev team.

## License
This package contains code licensed under the Apache License, Version 2.0 (the "License"). You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0 and may also view the License in the LICENSE file within this package.

[img-travis-master]: https://travis-ci.org/open-identity-fabric/open-identity-ios-sdk.svg
[url-travis-master]: https://travis-ci.org/open-identity-fabric/open-identity-ios-sdk

[img-coveralls-master]: https://coveralls.io/repos/github/open-identity-fabric/open-identity-ios-sdk/badge.svg?branch=master
[url-coveralls-master]: https://coveralls.io/github/open-identity-fabric/open-identity-ios-sdk?branch=master

[img-codacy]: https://api.codacy.com/project/badge/Grade/a070a59f6eaf43df9bf777de3899609a
[url-codacy]: https://app.codacy.com/gh/open-identity-fabric/open-identity-ios-sdk/dashboard

[img-jitpack]: https://jitpack.io/v/open-identity-fabric/open-identity-ios-sdk.svg
[url-jitpack]: https://jitpack.io/#open-identity-fabric/open-identity-ios-sdk

[img-license]: https://img.shields.io/github/license/open-identity-fabric/open-identity-ios-sdk.svg

[url-bintray]: https://bintray.com/open-identity-fabric/open-identity-ios-sdk

[img-github-watchers]: https://img.shields.io/github/watchers/open-identity-fabric/open-identity-ios-sdk.svg?style=social&label=Watch
[url-github-watchers]: https://github.com/open-identity-fabric/open-identity-ios-sdk/watchers
[img-github-stars]: https://img.shields.io/github/stars/open-identity-fabric/open-identity-ios-sdk.svg?style=social&label=Star
[url-github-stars]: https://github.com/open-identity-fabric/open-identity-ios-sdk/stargazers
[img-github-forks]: https://img.shields.io/github/forks/open-identity-fabric/open-identity-ios-sdk.svg?style=social&label=Fork
[url-github-forks]: https://github.com/open-identity-fabric/open-identity-ios-sdk/network



