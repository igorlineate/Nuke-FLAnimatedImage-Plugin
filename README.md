<p align="center"><img src="https://cloud.githubusercontent.com/assets/1567433/6684993/5971ef08-cc3a-11e4-984c-6769e4931497.png" height="100"/>

<p align="center">
<a href="https://cocoapods.org"><img src="https://img.shields.io/cocoapods/v/Nuke-Alamofire-Plugin.svg"></a>
<a href="https://github.com/Carthage/Carthage"><img src="https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat"></a>
</p>

[FLAnimatedImage](https://github.com/Flipboard/FLAnimatedImage) plugin for [Nuke](https://github.com/kean/Nuke) that allows you to load and display animated GIFs.

## Usage

#### Create Image Manager

```swift
// Use AnimatedImageDecoder and AnimatedImageLoaderDelegate
let decoder = ImageDecoderComposition(decoders: [AnimatedImageDecoder(), ImageDecoder()])
let loader = ImageLoader(configuration: ImageLoaderConfiguration(dataLoader: <#dataLoader#>, decoder: decoder), delegate: AnimatedImageLoaderDelegate())
ImageManager.shared = ImageManager(configuration: ImageManagerConfiguration(loader: loader))
```

#### Use Image View

```swift
let imageView = AnimatedImageView() // Nuke.ImageView subclass
imageView.setImageWithRequest(<#imageRequest#>)
```

#### Use Image Decoder

```swift
let animatedImage = AnimatedDecoder().imageWithData(<#data#>) // Nuke.AnimatedImage is created
let imageView = AnimatedImageView() // Nuke.ImageView subclass
imageView.displayImage(animatedImage) // Animated GIF playback is started
```

## Installation

See [Nuke](https://github.com/kean/Nuke) for installation instructions.

## Requirements
- iOS 8.0+
- Xcode 7.0+, Swift 2.0+

## Contacts

<a href="https://github.com/kean">
<img src="https://cloud.githubusercontent.com/assets/1567433/6521218/9c7e2502-c378-11e4-9431-c7255cf39577.png" height="44" hspace="2"/>
</a>
<a href="https://twitter.com/a_grebenyuk">
<img src="https://cloud.githubusercontent.com/assets/1567433/6521243/fb085da4-c378-11e4-973e-1eeeac4b5ba5.png" height="44" hspace="2"/>
</a>
<a href="https://www.linkedin.com/pub/alexander-grebenyuk/83/b43/3a0">
<img src="https://cloud.githubusercontent.com/assets/1567433/6521256/20247bc2-c379-11e4-8e9e-417123debb8c.png" height="44" hspace="2"/>
</a>

## License

Nuke is available under the MIT license. See the LICENSE file for more info.
