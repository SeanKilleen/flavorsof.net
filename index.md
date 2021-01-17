---
layout: single
author: Sean Killeen
author_profile: false
toc: true
toc_label: Contents
tock_sticky: true
title: "The Many Flavors of .NET"
---

I've often been asked about the differences between different incarnations of .NET and the differences between them. I created this guide to attempt to distill them.

## At a Glance

* **.NET 5** is the latest incarnation of .NET. It is the next evolution of .NET Core, and represents a branding consolidation.
  * **Do we say 'core'?**: .NET 5 does not include the word `Core` in its naming. However, ASP.NET 5 may also be called `ASP.NET Core 5` to distinguish from .NET MVC (which had a version 5). Similarly, certain libraries, e.g. Entity Framework, will call themselves `EF Core 5` to distinguish from `EF 5`, an older version of Entity Framework for .NET.
* **.NET Core** is the more recently developed successor to .NET Framework. Its last version is `v3.1`; it then becomes `.NET 5`.
* **.NET Standard** is a sort of contract that guarantees API surface to be available and thus limits where devices can run. It allows apps to target certain environments and know certain API calls are supported. `v2.1` is the last version, retired in favor of the way .NET 5 does targeting.
* **.NET Framework** is the original `.NET` -- the last version is `v4.8`. The future is `.NET 5`.

## The Various Flavors of .NET

Generally ordered from latest to earliest.

### .NET 6

This will be the first LTS (long-term support) release of .NET after going all in on .NET Core and moving to the `.NET` (eg. `.NET 5`) brand. At this point, Microsoft aims for the platform to have feature parity with Xamarin and Mono.

### .NET 5

With .NET 5, Microsoft says goodbye to .NET Framework, and goes "all in" on .NET Core. 

.NET 5 _is_ .NET Core, with a new name that makes it the standard-bearer. It is the natural evolution of .NET Core 3.1 with greater support and a broader surface area of compatibility.

.NET 5 is an active release and is not long-term support (LTS); for LTS support, users may need to wait for .NET 6.

### .NET Core

This is the newer edition of .NET that brings cross-platform support and a number of enhancements and changes. It was built from the ground up with the intention of re-thinking .NET for modern development workflows.

Microsoft is retiring the .NET Core brand in favor of unifying under .NET 5, which goes all in on .NET Core. The last version of .NET core will be v3.1 (the current LTS release).

### .NET Standard

.NET Standard is a little more abstract than other flavors mentioned here, but is included because the naming sometimes gets folks mixed up.

While the other flavors of .NET listed here are runtimes that turn your assemblies into running code, you can think of .NET Standard as a specification for which calls a program can make that will be supported by the underlying OS. The idea is that lower versions of .NET Standard will have a smaller API surface available to use, but will be able to run in more places. As the version numbers of .NET Standard increase, so does the API surface, but the number of places it can run is reduced.

.NET Standard is frozen as of v2.1 -- with the move to .NET 5, targeting is being done slightly differently.

* [Demystifying .NET Core and .NET Standard, by Immo Landwerth](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/september/net-standard-demystifying-net-core-and-net-standard)
* [.NET Standard on MS Docs](https://docs.microsoft.com/en-us/dotnet/standard/net-standard)

### Mono

Mono is one of the original open-source implementation of the .NET Framework, and led the way in cross-platform capabilities.

Microsoft's goal for .NET 5 was to incorporate the full capabilities of Mono, but that unification will be complete with .NET 6

* [Mono Project](https://www.mono-project.com/)

### Xamarin

Xamarin is the original cross-platform mobile application toolkit that aimed to bring .NET Capabilities with a unified experience to iOS, Android, etc.

Microsoft's goal for .NET 5 was to incorporate the full capabilities of Xamarin, but that unification will be complete with .NET 6

* [Xamarin](https://dotnet.microsoft.com/apps/xamarin)

### .NET Framework (a.k.a .NET, netfx)

This is the classic .NET Framework that has evolved through the years. 

The last developed version of the .NET Framework is v4.8. The future is in `.NET 5`, which evolved from `.NET Core`.

## FAQ

### Q: How does .NET 5 Work with .NET Standard?

.NET Standard will remain in use with .NET Core, but .NET 5 targets projects a little differently.

Rather than targeting a .NET Standard version, .NET 5 apps will target `net5.0` for code that runs everywhere, and `net5.0-windows` / `net5.0-android` etc. for code that needs a wider API surface and will run on a specific platform.

* [.NET 5 and .NET Standard -- MS Docs](https://docs.microsoft.com/en-us/dotnet/standard/net-standard#net-5-and-net-standard)
* [.NET 5 OS Specific TFMs -- MS Docs](https://docs.microsoft.com/en-us/dotnet/standard/frameworks#net-5-os-specific-tfms)

### Q: Who are you?

A: I'm [Sean Killeen](https://SeanKilleen.com), a Microsoft MVP and avid .NET developer. I had explained this to folks a few times so I figured I'd create a reference.

### Q: I don't think something on this site is correct.

A: [Issues](https://github.com/SeanKilleen/flavorsof.net/issues) and [Pull Requests](https://github.com/SeanKilleen/flavorsof.net/pulls) welcome! I'm always up for adding resources and making this page clearer.

### Q: In your opinion, Isn't this naming stuff absolute madness?

A: Naming things is hard, and I'm not one to judge. 

I think as future versions of .NET are released and potentially conflicting names drift into the past, it will become much easier. In my opinion Microsoft was in a tough spot; they had to distingiush from .NET Framework v4.8, have minimal conflicting names with other libraries, and attempt to unite the .NET ecosystem around one path forward in terms of names. There were several possible approaches and I can't say I thought any others would be better than this one.

## More Resources

Coming soon. Feel free to [suggest some](https://github.com/SeanKilleen/flavorsof.net/issues/new)!
