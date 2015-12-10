---
layout: post
title:  "Brake Pedal - rate limiting, throttling, and locking"
date:   2015-11-30 00:00:01
author: omar
---
`Brake Pedal` is a general purpose throttling and rate limting library for `.NET`. The code was forked from [WebApiThrottle](https://github.com/stefanprodan/WebApiThrottle). 
It's currently in use by our production systems. The library is available at [github.com/gopangea/BrakePedal](https://github.com/gopangea/BrakePedal). 

The core library provides the following features:

- Throttling: limit `X attempts` over `Y time period`.
- Locking: after `X attempts` over `Y time period` block future attempts for `Z time period`.

The library is composed of three packages:

- `BrakePedal` is the main package that contains all the logic as well as an in-memory repository.
	- [nuget.org/packages/BrakePedal](https://www.nuget.org/packages/BrakePedal)
- `BrakePedal.Http` contains code to use the main package in a web application as an handler or filter.
	- [nuget.org/packages/BrakePedal.Http](https://www.nuget.org/packages/BrakePedal.Http)
- `BrakePedal.Redis` contains an implementation of a Redis throttle repository which uses [StackExchange.Redis](https://github.com/StackExchange/StackExchange.Redis).
	- [nuget.org/packages/BrakePedal.Redis](https://www.nuget.org/packages/BrakePedal.Redis)

#### What's with the name?

The main purpose of this library is to "throttle". "Throttle" as a library name would be too generic. "Throttle" is also commonly used to refer to a car's gas pedal. However, "Gas Pedal" generally means increasing the speed, but this library is trying to limit speeds. "Brake Pedal" better denotes the purpose of the library. 

Sticking to the whole car analogy, maybe calling it "Cops" or "Police" would make more sense since the police would stop you if you go over the speed limit (throttling) and arrest you disallowing you to drive (locking)..?

If you'd like to suggest a name change, feel free to open a PR.

Enjoy!