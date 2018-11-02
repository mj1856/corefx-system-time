# .NET System.Time Project Repo

This repo is a fork of the [corefxlab](https://github.com/dotnet/corefxlab), with only the `System.Time` project.  Development of `System.Time` is done in this repo, and then pushed  upstream to corefxlab as necessary.

## System.Time Project Description

This project augments the date and time APIs in .NET.  It adds two new primitives to the `System` namespace:

### `Date`

This structure represents a whole date, having a year, month and day component.  It is ideal for representing or conveying a date without reference to time or time zone, such as a birth date.

#### Usage example

```csharp
Date d = new Date(2018, 12, 31);
```

Note that the methods and properties are similar to their counterparts in the [`DateTime`](https://docs.microsoft.com/dotnet/api/system.datetime) structure, with the key difference being that there is no representation of *time* or *kind*.

### `Time`

This structure represents a time of day, as would be read from a clock, within the range `00:00:00` to `23:59:59.9999999` (inclusive).  It is ideal for representing or conveying a time without reference to time zone or date, such as the time of a daily recurring appointment, or the scheduled opening and closing hours of a business on a given day of the week.

It is *not* intended to be used to represent a duration of elapsed time.  That scenario is already covered by the [`TimeSpan`](https://docs.microsoft.com/dotnet/api/system.timespan) structure.

#### Usage examples

```csharp
// 3:00 PM, using a 12 hour-clock
Time t1 = new Time(3, 0, Meridiem.PM);

// 15:00, using a 24 hour-clock
Time t2 = new Time(15, 0);

// (t1 == t2)
```

Note that the methods and properties are similar to their counterparts in the [`DateTime`](https://docs.microsoft.com/dotnet/api/system.datetime) structure, with the key difference being that there is no representation of *date* or *kind*.

## Installation Instructions

TBD

## Project Status / History

TBD

## Contributing

TBD

## Changelog

TBD
