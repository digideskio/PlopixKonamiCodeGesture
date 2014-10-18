Plopix Konami Code Gesture
==========================

Simple implementation of the KonamiCode gesture in Swift. 

Code: Up, Up, Down, Down, Left, Right, Left, Right, Tap, Tap

Including into your project
---------------------------

Just drag and drop PlopixKonamiGesture.swift file into your project.

The UIGestureRecognizerSubclass.h extension header is not included in the UIKit Swift framework. In order to compile code that uses those methods, you have to #import that header file inside an Objective-C Bridging Header for your Xcode project.

So don’t forget to add the #import statement in your *-Bridging-Header.h

	#import <UIKit/UIGestureRecognizerSubclass.h>
	
If you don't already have a bridge header file in your app, the easiest way to get one is to add an Obj-c class into your project, and Xcode will ask if you want to add one. You can then delete the Obj-c class.


Usage
-----

	override func viewDidLoad() {
        super.viewDidLoad()
        let recognizer = PlopixKonamiGesture(target: self, action: "launchEasterEgg:")
        view.addGestureRecognizer(recognizer)        
    }
    
    func launchEasterEgg(recognizer: UITapGestureRecognizer) {
        if ( recognizer.state == .Ended ) {
			// do what you want
        }
    }

You can also look at the example projet.


Contact
-------
Author: Sébastien Morel aka Plopix

Follow [@plopix](http://twitter.com/plopix) on Twitter for the latest news.

License
------------
Available under the MIT license. See the LICENSE file for more info.
