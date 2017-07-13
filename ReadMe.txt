Input Board App Type-1

steps:

1. create an App , use Swift, no storyboard, no document.
2. in MainMenu.xib, in Window, add a Text View.
3. in MainMenu.xib, in Objects->Delegate->Referencing Outlets, add a New ,
    drag to the Text View, it will create a connection. 
4. add a Swift file named MyTextView.swift, content:

import Cocoa
import Foundation
import InputMethodKit
class MyTextView : NSTextView  {
override func keyDown(with event: NSEvent) {
	Swift.print("MyTextView-keyDown:"+event.characters! as String)
	super.keyDown(with: event)
}
}

5. return to MainMenu.xib, find TextView, modify its Class as MyTextView.
6. run, then comes a window.
7. type your keyboard, and see Xcode's log window, IT WORKS !

