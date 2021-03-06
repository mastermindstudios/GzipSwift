
GzipSwift
========================

[![Swift](https://img.shields.io/badge/Swift-3.0-blue.svg)]()
[![platform](https://img.shields.io/badge/platform-macOS | iOS | watchOS | tvOS-blue.svg)]()
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Build Status](https://img.shields.io/travis/1024jp/GzipSwift/master.svg?style=flat)](https://travis-ci.org/1024jp/GzipSwift)
[![codecov.io](https://codecov.io/gh/1024jp/GzipSwift/branch/Swift3/graphs/badge.svg)](https://codecov.io/gh/1024jp/GzipSwift)
[![License](https://img.shields.io/github/license/1024jp/GzipSwift.svg)](https://github.com/1024jp/GzipSwift/blob/develop/LICENSE)

__GzipSwift__ is a framework with an extension of Data written in Swift. It enables compress/decompress gzip using zlib.

- __Requirements__: OS X 10.9 / iOS 8 / watchOS 2 / tvOS 9 or later
- __Swift version__: Swift 3.0


## Usage

```swift
import Gzip

// gzip
let compressedData: Data = try! data.gzipped()
let optimizedData: Data = try! data.gzipped(level: .bestCompression)

// gunzip
let decompressedData: Data
if data.isGzipped {
    decompressedData = try! data.gunzipped()
} else {
    decompressedData = data
}

// check data is gzipped
print(compressedData.isGzipped)
```


## Installation

1. Build Gzip framework.
3. In *Build Phases*, add `Gzip.framework` library to your project.
    <br /><img src="Documentation/binary_link@2x.png" height="150"/>
5. `import Gzip` in your Swift file.
6. Use in your code.

### Build via Carthage
GzipSwift is Carthage compatible. You can easily build GzipSwift adding the following line to your Cartfile.

```ruby
github "1024jp/GzipSwift" "swift3" ~> 3.0.0
```

## Lisence

© 2014-2016 1024jp

GzipSwift is distributed under the terms of the __MIT License__. See [LISENCE](LISENCE) for details.
