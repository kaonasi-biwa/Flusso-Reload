# Flusso Reload
<img src="https://github.com/kaonasi-biwa/Flusso-Reload/blob/main/images/Flusso_Re.png?raw=true" height=120px><br>  
Flusso Reloadは、Flusso Legacyをもとに作られたものです。  
要するに、後継って話です。  
ちゃんと許可は取ってますよ！！  

## 使い方
基本的には普通のブラウザと同じです。  
URL打ったり検索したり...

## 既知のバグ
起動して最初にでてくるウェブページが少し下にずれていることがある  
→SharpBrowserもしくはC#の問題です  
　なんとかしようとはしてるんですけど...

## bin.zipについて
src/binの容量がでかすぎるので、zip化されてます。  
派生を作りたいなら、bin.zipを解凍すればいいと思います。

## クレジット
Flusso Legacyの製作者さんの、[ざーく(@Firefox_ESR)](https://twitter.com/Firefox_ESR)さん  
アイコンの製作者さんの、[めろんわ～くす(@mwxdxx)](https://twitter.com/mwxdxx)さん  
SharpBrowserの製作者の皆様  
CefSharpの製作者の皆様  
ありがとうございました  
  
世界は優しい人達でできている...

# Flusso Reload(SharpBrowser)のReadMe

![SharpBrowser](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/logo3.png)

SharpBrowser is the fastest open source C# web browser there is! Slightly faster than Google Chrome when rendering web pages due to lightweight CEF renderer. We compared every available .NET browsing browsing engine and finally settled on the high-performance [CefSharp](https://github.com/cefsharp/CefSharp/). Released under the permissive MIT license.

## Features

- HTML5, CSS3, JS, HTML5 Video, WebGL 3D, etc
- Tabbed browsing
- Address bar (also opens Google)
- Back, Forward, Stop, Refresh
- Developer tools
- Search bar (also highlights all instances)
- Download manager
- Custom error pages
- Custom context menu
- Easily add vendor-specific branding, buttons or hotkeys
- View online & offline webpages

## Hotkeys

Hotkeys | Function
------------ | -------------
Ctrl+T		| Add a new tab
Ctrl+N		| Add a new window
Ctrl+W		| Close active tab
F5			| Refresh active tab
F12			| Open developer tools
Ctrl+Tab	| Switch to the next tab
Ctrl+Shift+Tab	| Switch to the previous tab
Ctrl+F		| Open search bar (Enter to find next, Esc to close)


## System requirements

- You need [VC++ 2015 Runtime](https://www.microsoft.com/en-in/download/details.aspx?id=48145) 32-bit and 64-bit versions

- You need .NET Framework 4.6.

- You need to install the version of VC++ Runtime that CEFSharp needs. Since we are using CefSharp 89, according to [this](https://github.com/cefsharp/CefSharp/#release-branches) we need the above versions


## Getting started

1. Download the project as a ZIP from Github

2. You need to unpack **`src\bin.zip`** to create the `src\bin` folder which contains important CefSharp binaries. The project will not work properly without this!

3. Open the main solution `SharpBrowser.sln` and run it.

4. If you have any issues with CefSharp, delete all the files in the `bin` folder (except the `storage` subfolder) and run a Nuget restore by building (F5) or manually restoring (`nuget restore` command).


## Code

- SharpBrowser uses CefSharp 89 and is built on NET Framework 4.6
- SharpBrowser supports AnyCPU as well as x86/x64 specific builds
- `MainForm.cs` - main web browser UI and related functionality
- `Handlers` - various handlers that we have registered with CefSharp that enable deeper integration between us and CefSharp
- `Data/JSON.cs` - fast JSON serializer/deserializer
- `bin` - Binaries are included in the `bin` folder due to the complex CefSharp setup required. Don't empty this folder.
- `bin/storage` - HTML and JS required for downloads manager and custom error pages

## Credits

- [Robin Rodricks](https://github.com/robinrodricks) - SharpBrowser project.
- [Alex Maitland](https://github.com/amaitland) - CefSharp project, wrapper for CEF embeddable browser.
- [Ahmet Uzun](https://github.com/postacik) - Original browser project.

## Screenshots

### Apple Homepage

![](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/1.png)

### Google Maps

![](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/2.png)

### Search Bar

![](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/search.png)

### Downloads Tab

![](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/3.png)

### Developer Tools

![](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/4.png)

### Custom Error Pages

![](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/error1.png)

![](https://github.com/sharpbrowser/SharpBrowser/raw/master/images/error2.png)

