DTAlertView
===========
![Perview 1](https://raw.github.com/Darktt/DTAlertView/master/Raw/Image/Perview1.png)![Perview 2](https://raw.github.com/Darktt/DTAlertView/master/Raw/Image/Perview2.png)

Custom alert view to solved the UIAlertView can't addSubview problem on iOS7.

##ATTENTION##

* This demo code create on **Xcode 5.0**, but probably have issues on **Xcode 4 or less**.
* Demo code use at **non-ARC** mode, but **DTAlertView** main class support **ARC** and **non-ARC** mode.

##Installation##

1. Add `QuartzCore` framework.
2. Drag the `DTAlertView` folder into your project.

##Usage##

Import the header file and declare in want to used class.

	#import "DTAlertView.h"
	
###Initializing DTAlertView in your class:###

``` objective-c
// initial for class method
DTAlertView *alertView = [DTAlertView alertViewWithTitle:@"Demo" message:@"This is normal alert view." delegate:nil cancelButtonTitle:@"Cancel" positiveButtonTitle:@"OK"];

// inital for instance method
DTAlertView *alertView = [[DTAlertView alloc] initWithTitle:@"Demo" message:@"This is normal alert view." delegate:nil cancelButtonTitle:@"Cancel" positiveButtonTitle:@"OK"];
```

and you can use **Block** with alert view:

``` objective-c
DTAlertViewButtonClickedBlock block = ^(DTAlertView *_alertView, NSUInteger buttonIndex, NSUInteger cancelButtonIndex){
	// You can button title of clicked button.
    NSLog(@"%@", _alertView.clickedButtonTitle);
};

DTAlertView *alertView = [DTAlertView alertViewUseBlock:block title:@"Demo" message:@"This is normal alert view with block." cancelButtonTitle:@"Cancel" positiveButtonTitle:nil];
```

###Show & dismiss:###

Show alert view:

``` objective-c
[alertView show];
```
<!--
// Show alert view use custom animation.
[alertView showWithAnimationBlock:^{
	// Implemnet your custom animation code
	
}];
-->

Dismiss alert view:

``` objective-c
[alertView dismiss];
```

##License##
Licensed under the Apache License, Version 2.0 (the "License");  
you may not use this file except in compliance with the License.  
You may obtain a copy of the License at

>[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
 
Unless required by applicable law or agreed to in writing,  
software distributed under the License is distributed on an  
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,  
either express or implied.   
See the License for the specific language governing permissions  
and limitations under the License.