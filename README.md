# Leanplum-tvOS-SDK

[block:callout]
{
  "type": "warning",
  "body": "It's important to note that official support for tvOS is limited. However, if you are trying to use Leanplum on a tvOS application, continue below for an example of how you can integrate the LeanplumTV SDK."
}
[/block]
The following setup guide uses Cocapods. This is a sample integration framework on how you can implement the Leanplum tvOS SDK. 
[block:api-header]
{
  "type": "basic",
  "title": "1. Assumptions"
}
[/block]
We are assuming that you already have `cocoapods` installed. If not, follow the setup instructions for the Leanplum iOS SDK [Install our SDK](doc:install-our-sdk) 
[block:api-header]
{
  "title": "2. Edit your podspec"
}
[/block]
Navigate into your project and open the `Podspec` file:

`open -a Xcode Podfile`

Add the Leanplum tvOS pod by adding this line into your Podspec:

`pod 'Leanplum-tvOS-SDK', '~> 2.0'`
[block:api-header]
{
  "title": "3. Install your pods"
}
[/block]
Now, install the Leanplum SDK pods by running the following command:

Run: `pod install`

[block:api-header]
{
  "title": "4. Edit your AppDelegate"
}
[/block]
Make sure to import the `LeanplumTV` framework:

`#import <LeanplumTV/Leanplum.h>`
[block:code]
{
  "codes": [
    {
      "code": "#import \"AppDelegate.h\"\n#import <LeanplumTV/Leanplum.h>\n\n@implementation AppDelegate\n\n- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions\n{\n  // Insert your API keys here.\n  #ifdef DEBUG\n    LEANPLUM_USE_ADVERTISING_ID;\n    [Leanplum setAppId:@\"YOUR_APP_ID\"\n     withDevelopmentKey:@\"YOUR_DEVELOPMENT_KEY\"];\n  #else\n    [Leanplum setAppId:@\"YOUR_APP_ID\"\n     withProductionKey:@\"YOUR_PRODUCTION_KEY\"];\n  #endif\n\n  // Starts a new session and updates the app content from Leanplum.\n  [Leanplum start];\n  return YES;\n}\n...\n\n@end",
      "language": "objectivec"
    }
  ]
}
[/block]

[block:api-header]
{
  "title": "Example Project"
}
[/block]
An example project with the tvOS SDK installed can be found here: 

[Leanplum-tvOS-SDK-Example](https://github.com/Leanplum/Leanplum-tvOS-SDK-Example)

And if you're curious the podspec can be found here: 

[Leanplum-tvOS-SDK.podspec](https://github.com/Leanplum/Leanplum-tvOS-SDK/blob/master/Leanplum-tvOS-SDK.podspec)
