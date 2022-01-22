**SharpAvi** is a simple .NET library for creating video files in AVI format.

If you want to render some video sequence, but do not want to touch native APIs like DirectShow or to depend on command-line utilities like FFmpeg then **SharpAvi** may be what you need.
Writing uncompressed AVI does not require any external dependencies, it's a pure .NET code.
Files are produced in compliance with the [OpenDML extensions](http://www.jmcgowan.com/avitech.html#OpenDML) which allow (nearly) unlimited file size (no 2GB limit).

A video is created by supplying individual in-memory bitmaps and audio samples.
There are some built-in encoders for video and audio.
Output format is always AVI, regardless of a specific codec used.

The project is published to NuGet as a few packages:
* [SharpAvi](https://www.nuget.org/packages/SharpAvi/)  
  Contains core functions and some encoders which do not depend on external packages.
  * A Motion JPEG video encoder based on WPF. Supported in **net45** and **net50-windows** targets.
  * An MPEG-4 video encoder based on the Video for Windows (VFW) API. Supported in all targets when running on Windows.
  * [LAME](https://lame.sourceforge.io/)-based MP3 audio encoder. Supported in **net45**, **net50** and **net50-windows** targets.
* [SharpAvi.ImageSharp](https://www.nuget.org/packages/SharpAvi.ImageSharp/)  
  Contains a Motion JPEG video encoder based on [SixLabors.ImageSharp](https://github.com/SixLabors/ImageSharp).  
  It's a cross-platform alternative to the WPF-based encoder.

To get started, jump to the [project's wiki](https://github.com/baSSiLL/SharpAvi/wiki/Home).

***

A bit of history. This project has started on [CodePlex](https://sharpavi.codeplex.com/) in 2013. Then the repository was mirrored to GitHub for some time, until the project has been moved to GitHub completely in the middle of 2017.
