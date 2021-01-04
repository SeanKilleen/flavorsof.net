# The Flavors of .NET

A quick reference for the sometimes-confusing differences in .NET nomenclature.

## Summary

* **.NET Framework** is the original `.NET` -- the last version is `v4.8`, in favor of `.NET 5`
* **.NET Core** is the more recently developed successor to .NET Framework. Its last version is `v3.1`; it then becomes `.NET 5`.
* **.NET Standard** is a sort of contract that guarantees API surface to be available and thus limits where devices can run. It allows apps to target certain environments and know certain API calls are supported. `v2.1` is the last version, retired in favor of the way .NET 5 does targeting.
* **.NET 5** (or .NET Core 5) is the latest incarnation of .NET. It is the next evolution of .NET Core, and represents a branding consolidation.
* **Do we say 'core'?**: .NET 5 may also be called `.NET Core 5` to distinguish from .NET MVC (which had a version 5). Similarly, certain libraries, e.g. Entity Framework, will call themselves `EF Core 5` to distinguish from `EF 5`, an older version of Entity Framework for .NET.

## .NET Framework (a.k.a .NET, netfx)

This is the classic .NET Framework that has evolved through the years. 

The last developed version of the .NET Framework is v4.8.

## .NET Core

This is the newer edition of .NET that brings cross-platform support and a number of enhancements and changes. It was built from the ground up with the intention of re-thinking .NET for modern development workflows.

Microsoft is retiring the .NET Core brand in favor of unifying under .NET 5, which goes all in on .NET Core. The last version of .NET core will be v3.1 (the current LTS release).

## .NET Standard

You can think of .NET Standard as an specification for which calls a program can make that will be supported by the underlying OS. The idea is that lower versions of .NET Standard will have a smaller API surface available to use, but will be able to run in more places. As the version numbers of .NET Standard increase, so does the API surface, but the number of places it can run is reduced.

.NET Standard is frozen as of v2.1 -- with the move to .NET 5, targeting is being done slightly differently.

* [Demystifying .NET Core and .NET Standard, by Immo Landwerth](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/september/net-standard-demystifying-net-core-and-net-standard)
* [.NET Standard on MS Docs](https://docs.microsoft.com/en-us/dotnet/standard/net-standard)

## .NET 5

With .NET 5, Microsoft says goodbye to .NET Framework, and goes all in on .NET Core. 

.NET 5 _is_ .NET Core, with a new name that makes it the standard-bearer. It is the natural evolution of .NET Core 3.1 with greater support.

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
