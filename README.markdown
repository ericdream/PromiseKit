![PromiseKit](http://promisekit.org/public/img/logo-500.png)

Modern development is highly asynchronous: isn’t it about time we had tools that made programming asynchronously powerful, easy and delightful?

```swift
firstly {
    UIApplication.shared().networkActivityIndicatorVisible = true
}.then {
    when(fetchImage(), getLocation())
}.then { image, location in
    self.imageView.image = image;
    self.label.text = "Buy your cat a house in \(location)"
}.always {
    UIApplication.shared().networkActivityIndicatorVisible = false
}.catch { error in
    UIAlertView(/*…*/).show()
}
```

PromiseKit is a thoughtful and complete implementation of promises for iOS and macOS with first-class support for **both** Objective-C *and* Swift.

![](https://img.shields.io/cocoapods/v/PromiseKit.svg?label=Current%20Release)  [![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg)](https://github.com/Carthage/Carthage)
[![codebeat](https://codebeat.co/badges/6a2fc7b4-cc8f-4865-a81d-644edd38c662)](https://codebeat.co/projects/github-com-mxcl-promisekit)
[![Join the chat at https://gitter.im/mxcl/PromiseKit](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mxcl/PromiseKit?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# Getting Setup

```ruby
#CocoaPods
pod "PromiseKit", "~> 4.0"

#Carthage
github "mxcl/PromiseKit" ~> 4.0
```

Or, clone the project and drag and drop its `xcodeproj` into your Xcode project.

# Learning The Ropes

* Check out our complete, comprehensive [PromiseKit documentation](http://promisekit.org/docs/).

Neither CocoaPods or Carthage will install PromiseKit 2, 3 or 4 for an iOS 7 target. You need PromiseKit 1.7:

    pod "PromiseKit", "~> 1.7"

PromiseKit 1.7 has only limited Swift support.

# PromiseKit vs. Xcode

PromiseKit contains Swift, so we engage in an unending battle with Xcode:
>>>>>>> Compiles with Xcode 8 beta3

* Xcode 8 = PromiseKit 4
* Xcode 7 = PromiseKit 3
* Xcode 6 = PromiseKit 2

PromiseKit 1 is pure Objective-C and we still maintain it.

# Support

PromiseKit is lucky enough to have a large community behind it which is reflected in our [Gitter chat](https://gitter.im/mxcl/PromiseKit). If you're new to PromiseKit and are stumped or otherwise have a question that doesn't feel like an issue (and isn't answered in our [documentation](http://promisekit.org/introduction)) then our Gitter is a great place to go for help. Of course if you're onto something that you believe is broken or could be improved then opening a new issue is still the way to go 👍.

# Donations

PromiseKit is hundreds of hours of work almost completely by just me: [Max Howell](https://twitter.com/mxcl). I thoroughly enjoyed making PromiseKit, but nevertheless if you have found it useful then your bitcoin will give me a warm fuzzy feeling from my head right down to my toes: 1JDbV5zuym3jFw4kBCc5Z758maUD8e4dKR.

# License

Copyright 2015, Max Howell; <mxcl@me.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
