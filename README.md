# dotnet-sdk-2.2.203-linux-arm64-NoICU  
当你在 Linux 或 docker 中安装 .NET Core 时，可能会出现 ICU 问题：  
ICU issues can occur when you install.net Core in Linux or docker：  

```Shell
FailFast:
Couldn't find a valid ICU package installed on the system. Set the configuration flag System.Globalization.Invariant to true if you want to run with no globalization support.

   at System.Environment.FailFast(System.String)
   at System.Globalization.GlobalizationMode.GetGlobalizationInvariantMode()
   at System.Globalization.GlobalizationMode..cctor()
   at System.Globalization.CultureData.CreateCultureWithInvariantData()
   at System.Globalization.CultureData.get_Invariant()
   at System.Globalization.CultureInfo..cctor()
   at System.StringComparer..cctor()
   at System.AppDomain.InitializeCompatibilityFlags()
   at System.AppDomain.CreateAppDomainManager()
   at System.AppDomain.Setup(System.Object)
Aborted (core dumped)
```
这个版本根据微软官网的版本修改，解决了 ICU 问题  
This version was modified according to the official website of Microsoft, and solved the ICU problem
