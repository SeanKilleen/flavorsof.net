# The Flavors of .NET

A quick reference for the sometimes-confusing differences in .NET Nomenclature.

## .NET Framework (a.k.a .NET, netfx)

This is the classic .NET Framework that has evolved through the years. 

The last developed version of the .NET Framework is v4.8.

## .NET Core

This is the newer edition of .NET that brings cross-platform support and a number of enhancements and changes. It was built from the ground up with the intention of re-thinking .NET for modern development workflows.

Microsoft is retiring the .NET Core brand in favor of unifying under .NET 5, which goes all in on .NET Core. The last version of .NET core will be v3.1 (the current LTS release).

* [Wikipedia: .NET Core](https://en.wikipedia.org/wiki/.NET_Core)

## .NET Standard

You can think of .NET Standard as an specification for which calls a program can make that will be supported by the underlying OS. The idea is that lower versions of .NET Standard will have a smaller API surface available to use, but will be able to run in more places. As the version numbers of .NET Standard increase, so does the API surface, but the number of places it can run is reduced.

## .NET 5

With .NET 5, Microsoft says goodbye to .NET Framework, and goes all in on .NET Core. 

.NET 5 _is_ .NET Core, and is the natural evolution of .NET Core 3.1 with greater support.

## FAQ

### Q: How does .NET 5 Work with .NET Standard?

TODO

### Q: Who are you?

A: I'm [Sean Killeen](https://SeanKilleen.com), a Microsoft MVP and avid .NET developer.

### Q: I don't think something on this site is correct.

A: [Issues](https://github.com/SeanKilleen/flavorsof.net/issues) and [Pull Requests](https://github.com/SeanKilleen/flavorsof.net/pulls) welcome! I'm always up for adding resources and making this page clearer.

## More Resources
