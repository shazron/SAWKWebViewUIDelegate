## SAWKWebViewUIDelegate
https://github.com/shazron/SAWKWebViewUIDelegate

A UIDelegate for WKWebView that is equal to the default UIDelegate behaviour in a UIWebView. iOS 8 only.


### Usage
```
WKWebViewConfiguration* configuration = [[WKWebViewConfiguration alloc] init];
configuration.userContentController = [[WKUserContentController alloc] init];

CGRect bounds = [[UIScreen mainScreen] bounds];
NSString* title = [[NSBundle mainBundle] objectForInfoDictionaryKey:@"CFBundleDisplayName"];

WKWebView* webView = [[WKWebView alloc] initWithFrame:bounds configuration:configuration];
```

####  Method 1 to initialize the UIDelegate, it will just use the rootViewController of the app

```
SAWKWebViewUIDelegate* uiDelegate = [[SAWKWebViewUIDelegate alloc] initWithTitle:title];
webView.UIDelegate = uiDelegate;
```
#### Method 2 to initialize the UIDelegate, specify a viewController

```
UIViewController* viewController = [UIApplication sharedApplication].delegate.window.rootViewController;
SAWKWebViewUIDelegate* uiDelegate = [[SAWKWebViewUIDelegate alloc] initWithTitle:title viewController:viewController];
webView.UIDelegate = uiDelegate;
```

### Issues

https://github.com/shazron/SAWKWebViewUIDelegate/issues

### License

Copyright [2014] Shazron Abdullah

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
