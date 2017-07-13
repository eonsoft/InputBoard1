Input Board App Type-1

a simple App handles your keyDown action.

steps:

1. create an App , use Swift, no storyboard, no document.
2. add a Swift file named MyTextView.swift, content:

import Cocoa
import Foundation
class MyTextView : NSTextView  {
override func keyDown(with event: NSEvent) {
Swift.print("MyTextView-keyDown:"+event.characters! as String)
super.keyDown(with: event)
}
}

3. in MainMenu.xib, in Window, add a Text View, modify its Class as MyTextView.
4. in MainMenu.xib, in Objects->Delegate->Referencing Outlets, add a New ,
    drag to the Text View, it will create a connection. 
5. run, then comes a window.
7. type your keyboard, and see Xcode's log window, IT WORKS !

