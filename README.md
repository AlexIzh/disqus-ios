# iOS Disqus API 

This open-source library allows you to integrate Disqus into your iOS apps. Learn more about [Disqus API](http://disqus.com/api/docs/).

The project has been created by Moqod team to help many developers searching for this solution on Stackoverflow and else where. Special thanks to Disqus for answering support questions promptly! When integrating this solution to your project, please, spare us a like on [Facebook](http://fb.me/moqod), follow us on [Twitter](http://twitter.com/moqod) or spread a good word about us!

Feel free to get in touch with us in regards to any questions or cooperation requests via email [info@moqod.com](mailto:info@moqod.com).

# Attention
- Please, note the library uses git submodules, so make sure you clone the submodules to be able to use the library.
- The project is non-ARC at the moment. To use it in your ARC-based projects add `-fno-objc-arc` flag to source files.


# Features
- Authorization via disqus.com.
- API access.
- Posting comments to discuss.
- Answering comments in a thread.
- And much more! Just learn the API and documentation.

# Todo
- Access token refresh.
- Customizable authorization user interface. 
- ARC support.
- Authorization via supported social networks (Facebook, Twitter, Google+)

# 3rd Libraries
This library uses [AFNetworking](https://github.com/AFNetworking/AFNetworking).

# Sample

``` objc
    MDDisqusComponent *disqusComponent = [[MDDisqusComponent alloc] initWithPublicKey:@"<YOUR_PUBLIC_KEY>"
        																	secretKey:@"<YOUR_SECRET_KEY>"
																		  redirectURL:[NSURL URLWithString:@"<YOUR_REDIRECT_URL>"]];
    
    [disqusComponent requestAPI:@"threads/list" params:@{@"forum" : @"<YOUR_FORUM_SHORTNAME>"} handler:^(NSDictionary *response, NSError *error) {
		if (nil == error) {
			NSLog(@"response == %@", response);
		} else {
			NSLog(@"error == %@", error);
		}
	}];
    

```

# License
MIT
