TeamCity-extensions
===================

## How to wrap TeamCity NUnit Runner with powershell? ##

Here is the example.

Run Platform\build\TestProduct\Impl\InTest\RunTests.ps1

- locally and nunit-console will be used
- at TeamCity and TeamCity runner will be used

When your build scripts are relativelly complicated, the ability to run the whole thing locally became very desirable.

## How to clone, power on/off, etc VmWare vitual machines? ##

1. Install [VMware vSphere PowerCLI](https://my.vmware.com/web/vmware/details?downloadGroup=VSP510-PCLI-510&productId=285).
2. Implement your own Platform\Tools\OsTestFramework.Config\OsTestFramework.GetConfig.ps1
3. Implement your own Platform\build\TestProduct\Impl\InTest\GetAssembliesToTest.ps1
4. Scripts require vCenter, free ESXi host will not be sufficient for linked clone feature.

This repository is a part of a [blog post series](http://dev-in-test.blogspot.com/2014/02/how-we-at-jetbrains-dotnet-team-do.html) about automation testing using JetBrains TeamCity and VmWare VCenter.