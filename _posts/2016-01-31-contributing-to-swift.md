---
layout: post
title: Contributing to Swift
---
Ever since Apple announced Swift I was pretty excited to get my hands on it, but since I'm not an iOS person, I waited for the open source version before really looking into it.

To my surprise Apple didn't just dump the code somewhere and called it a day but put it up on github, the whole history intact, and was actively merging the first wave of pull requests consisting of mostly typos fixes. To start learning Swift a friend and I decided to write a [little utility library](https://github.com/Memorion/BitUnits). While things started off great we began to hit some boundaries of the current state of the open source Swift ecosystem, namely that the XCTest library is currently not included in the snapshots which makes testing without XCode on OSX nigh impossible. 

Trying to circumvent the issue turned up another one, which is being tracked [here](https://bugs.swift.org/browse/SR-588). By now, having spent a not insignificant amount of time looking through the swift package manager source, I was confident enough to try and implement [this](https://bugs.swift.org/browse/SR-353) request for a `npm init` style feature and after several local revisions with a lot of help from [Tobias](https://github.com/tlandsberg) we felt brave enough to submit a pull request.

And after one tiny adjustment, refactoring the `--init` case into its own file it actually got [merged](https://github.com/apple/swift-package-manager/commit/9deed030f0ece93abf9587392c8cdf3bc15fc786)! It feels pretty cool to have written a tiny bit of code that ships with the swift-package-manager in the future. Although I wish git would provide a way to mark a commit for being worked on by multiple people because I'd rather share the credit with Tobias.

All in all I'm quite excited for Swift as a general purpose language and I can't wait for Version 3.0!
