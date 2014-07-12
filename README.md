## SAWKWebViewUIDelegate
https://github.com/shazron/SAWKWebViewUIDelegate

A UIDelegate for WKWebView that is equal to the default UIDelegate behaviour in a UIWebView. iOS 8 only.


### Usage
```
WKWebViewConfiguration* configuration = [[WKWebViewConfiguration alloc] init];
configuration.userContentController = [[WKUserContentController alloc] init];

WKWebView* webView = [[WKWebView alloc] initWithFrame:[[UIScreen mainScreen] bounds] configuration:configuration];
```

####  Method 1: uses CFBundleDisplayName for the title and the app rootViewController
```
SAWKWebViewUIDelegate* uiDelegate = [[SAWKWebViewUIDelegate alloc] init];
webView.UIDelegate = uiDelegate;
```

####  Method 2: specify the title and uses the app rootViewController
```
SAWKWebViewUIDelegate* uiDelegate = [[SAWKWebViewUIDelegate alloc] initWithTitle:@"MyAppTitle"];
webView.UIDelegate = uiDelegate;
```

####  Method 3: specify the title and specify the viewController
```
UIViewController* viewController = [UIApplication sharedApplication].delegate.window.rootViewController;
SAWKWebViewUIDelegate* uiDelegate = [[SAWKWebViewUIDelegate alloc] initWithTitle:@"MyAppTitle" viewController:viewController];
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
