[![Build Status](https://travis-ci.org/sduplooy/Notus.svg?branch=master)](https://travis-ci.org/sduplooy/Notus)
[![NuGet Badge](https://buildstats.info/nuget/Notus)](https://www.nuget.org/packages/Notus/)

# Notus

Provides a notification object that collects errors and warnings.

## NuGet
To install the package from NuGet, run the following command:
`Install-Package Notus`

## Usage

To add an *error* to the notification object:

```C#
new Notification().AddError("Policy number is missing");
//or
new Notification().AddError(new Error("Policy number is missing"));
```
To add a *warning* to the notification object:

```c#
new Notification().AddWarning("Amount is close to the lending limit");
//or
new Notification().AddWarning(new Warning("Amount is close to the lending limit"));
```

To check if  the notification has any *errors*:

```c#
new Notification().HasErrors();
```

To check if  the notification has any *warnings*:

```c#
new Notification().HasWarnings();
```

To check if the notification has a specific *error*:

```c#
new Notification().IncludesError("Policy number is missing");
```

To check if the notification has a specific *warning*:

```c#
new Notification().IncludesWarning("Amount is close to the lending limit");
```

See [Notification by Martin Fowler](https://martinfowler.com/eaaDev/Notification.html)
