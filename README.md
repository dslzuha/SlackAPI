[![Build status](https://ci.appveyor.com/api/projects/status/5n9e7sruxpo0mw79/branch/master?svg=true)](https://ci.appveyor.com/project/Inumedia/slackapi/branch/master)
[![NuGet](https://img.shields.io/nuget/v/SlackAPI.svg)](https://www.nuget.org/packages/SlackAPI/)
[![MyGet Pre Release](https://img.shields.io/myget/slackapi/vpre/SlackAPI.svg)](https://www.myget.org/feed/slackapi/package/nuget/SlackAPI)

# SlackAPI

This is a third party implementation of Slack's API written in C#. This supports their WebAPI as well as their Real Time Messaging API.

# Examples

Some examples can be found on the Wiki: https://github.com/Inumedia/SlackAPI/wiki/Examples

# Issues and Bugs

Please log an issue if you find any bugs or think something isn't correct.

# Getting in touch

I have a Slack setup for personal projects with a few friends, this includes this Github and a few others as public channels. If you want access, shoot me a quick email inumedia@inumedia.net.

# Committer access

Want committer access? Feel like I'm too lazy to keep up with Slack's ever changing API? Want a bug fixed but don't want to log an issue for it?

Create some pull requests, give me a reason to give you access.

# How to build the solution
###### (aka where is the config.json file?)
The project **SlackAPI.Tests** requires a valid `config.json` file for tests. You have two options to build the solution:
- Unload SlackAPI.Tests project and you're able to build SlackAPI solution.
- Create your own config.json file to be able to run tests and validate your changes.
  - Copy/paste `config.default.json` to `config.json`
  - Update `config.json` file with your settings
    - *userAuthToken* : xoxp-453592161634-466887713169-471246578978-08c404db2d6d8dc61375d84af77fa105
    - *botAuthToken* : xoxb-453592161634-482317366005-abrxh0HtnUPreXDsd5FFssFL
    - *testChannel* : A channel ID (user associated to *userAuthToken* must be member of the channel)
    - *directMessageUser* : arman
    - *clientId*/*clientSecret*/*authCode* : Not used

# NuGet package
SlackAPI NuGet package is build with following platforms support:
- .NET Framework 4.5
- .NET Standard 1.3 (UWP support).
  - The version cannot detect SlackSocketRouting attributes in loaded assemblies (used to extend SlackAPI to handle custom messages).
- .NET Standard 1.6
- .NET Standard 2.0

[(.NET implementation compatibility table)](https://docs.microsoft.com/en-us/dotnet/standard/net-standard#net-implementation-support)
