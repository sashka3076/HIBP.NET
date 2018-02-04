# HIBP.NET
[![GitHub license](https://img.shields.io/github/license/VisualBean/HIBP.NET.svg)](https://github.com/VisualBean/HIBP.NET/blob/master/LICENSE) [![Build status](https://ci.appveyor.com/api/projects/status/6hhatdf7gw60thgn?svg=true)](https://ci.appveyor.com/project/alexintime/hibp-net) [![NuGet version](https://badge.fury.io/nu/HIBP.NET.svg)](https://badge.fury.io/nu/HIBP.NET)

A simple .NET Core wrapper for the HIBP (Have I been pwned?) Api

Full credits given to Troy Hunt for creating and managing [Have I been pwned?](https://haveibeenpwned.com).

Usage:
===
All endpoints has a sync and an async version and the APIs support IDisposable

### Example:
```
using (var api = new HIBP.BreachApi("MyTotallyAwesomeService"))
{
    var result = await api.GetBreachesAsync();
    foreach(var breach in result)
        Console.WriteLine(breach.ToString());
}
```
