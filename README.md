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
SAWKWebViewUIDelegate* uiDelegate = [[SAWKWebViewUIDelegate alloc] initWithTitle:title viewController];
webView.UIDelegate = uiDelegate;
```

### Issues

https://github.com/shazron/SAWKWebViewUIDelegate/issues
