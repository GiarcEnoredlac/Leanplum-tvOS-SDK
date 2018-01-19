# Leanplum-tvOS-SDK

##It's important to note that official support for tvOS is limited. However, if you are trying to use Leanplum on a tvOS application, continue below for an example of how you can integrate the LeanplumTV SDK.

The following setup guide uses Cocoapods. This is a sample integration framework on how you can implement the Leanplum tvOS SDK. 

### Assumptions

We are assuming that you already have `cocoapods` installed. If not, follow the setup instructions for the Leanplum iOS SDK

### Edit your PodSpec
Navigate into your project and open the `Podspec` file:

`open -a Xcode Podfile`

Add the Leanplum tvOS pod by adding this line into your Podspec:

`pod 'Leanplum-tvOS-SDK', '~> 2.0'`

### update your Pods
Now, install the Leanplum SDK pods by running the following command:

Run: `pod install`
