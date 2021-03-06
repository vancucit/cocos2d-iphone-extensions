Cocos2d Extensions
=================
This repo is a collection of different 3rd party extensions for the Cocos2d-iPhone Engine.

How to get the source
=================
While gh-pages is main branch you need to execute this, to clone the repo and get to the extensions source: 

```
    git clone git@github.com:cocos2d/cocos2d-iphone-extensions.git
    cd cocos2d-iphone-extensions
    git fetch origin
    git checkout -t origin/master
    git submodule update --init
```

Files & Folders
=================
* **cocos2d** - cocos2d-iphone submodule.
* **Extensions** - folders with extensions sources, that can be inlcuded in your project.
* **Tests** - sources & resources of Extensions demos.
   * **SharedResources** - resources shared between all tests (icons, fps images, etc...)
   * **SharedSources** - sources shared between all tests (appDelegates, pch's, etc...)
* **cocos2d-extensions-ios.xcodeproj** - XCode Project containing all extensions and their demos/tests for iOS Platform.
* **cocos2d-extensions-mac.xcodeproj** - XCode Project containing all extensions and their demos/tests for Mac OS X Platform.

Extensions
=================
 * [iOS/Mac] **CCMenuAdvanced** - CCMenu subclass with additional features: relativeAnchor, more align options, priority property, scrolling with swipe/trackpad/mousewheel
 * [iOS/Mac] **CCMenuItemSpriteIndependent** - CCMenuItemSprite Subclass, that doesnt add normal/selected/disabled images (sprites) as children. It retains them and delegates rect & convertToNodeSpace: methods to normalImage_. So it's possible to use CCSpriteBatchNode & add position sprites of menuItem anyway you want.
 * [iOS/Mac] **CCVideoPlayer** - Simple Video Player for Cocos2D apps.
 * [iOS/Mac] **CCBigImage** - Dynamic Tiled Node for holding Large Images.
 * [iOS/Mac] **CCSlider** - Little Slider Control to allow the user to set the music/sfx/etc level in the range of 0.0f to 1.0f.
 * [iOS/Mac] **CCSendMessages** - CCActionInstant subclass, that is more flexible than other CCActions that run functions. Can be used in many cases as blocks replacement. 
 * [iOS] **CCScrollLayer** - CCLayer subclass that lets you pass-in an array of layers and it will then create a smooth scroller. Complete with the "snapping" effect.
 * [iOS/Mac] **FilesDownloader** - Downloader for a group of files with shared source path.
 
 Video Overview and more Info can be found on the [Wiki](https://github.com/cocos2d/cocos2d-iphone-extensions/wiki "Wiki")   
 Detailed README for each extension is available in it's folder (i.e. Extensions/CCSlider/README.md).   
 On the GitHub it will be automatically shown under files list in the extension folder.
 
Building & Running Tests
=========================
Agregate target "BuildAllTests" will build all extensions tests - just set it as active target and change only active excecutable to choose the test.   
Extension Test Template is used only as a template for new extensions test targets. It should not build, cause there's no ExtensionTest class implementation for this target.   
SYNTHESIZE_EXTENSION_TEST() macro is used (only once in each extension test) to implement ExtensionTest class, that creates scene with default extension test layer.
 
Contributing
================
Looking for Roadmap or TODO's? Check the [issues](https://github.com/cocos2d/cocos2d-iphone-extensions/issues "Issues") page.  
Want to share your own extension for cocos2d? Read this: [Adding-new-Extension](https://github.com/cocos2d/cocos2d-iphone-extensions/wiki/Adding-new-Extension)  
Know something that should be inlcuded in cocos2d-extensions-repo? Got problems and/or found a bug? [Create an Issue](https://github.com/cocos2d/cocos2d-iphone-extensions/issues/new "New Issue")
