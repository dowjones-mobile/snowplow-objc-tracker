Snowplow documentation:
  We forked Snowplow-objc-tracker framework as it includes swizzle code. 
It overrides viewDidAppear and we want to bypass this and call the “record event” at some other point of the lifecycle

What we have changed is we do not override viewDidAppear method of UIViewController.
 Instead we have `trackSnowPlowEvent` method available for UIViewController which contains the same code as what was previously in SP_viewDidAppear method,
