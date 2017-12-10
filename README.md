# DemoCefBrowser
A demo implemtation of [phi-el/CefBrowser](https://github.com/phi-el/CefBrowser) (CefSharp w/ automation possibilities)
**clone with: 'git clone --recursive https://github.com/phi-el/DemoCefBrowser.git'**
Ensure that you have installed .net v4.5.2 before opening any solution file!

## Steps made to get CefBrowser working
 - cd into the directory and "git clone https://github.com/phi-el/CefBrowser.git"
 - check dependencies of CefBrowser (@ the moment: [ExceptionHandling](https://github.com/phi-el/ExceptionHandling), [EncodingEx](https://github.com/phi-el/EncodingEx), [HashingEx](https://github.com/phi-el/HashingEx), [RPC-Communication](https://github.com/phi-el/rpc-communication-net2), [SerializationDotNet2](https://github.com/phi-el/SerializiationDotNet2), [IoHelper](https://github.com/phi-el/IoHelper)), 
 - clone the dependencies to the root folder, so that CefBrowser and the others are in the same folder where you will create your unique project
 - open each .sln file in vs-studio, recover nuget-packages, open CefBrowser at the end!
 - close all projects
 - create vs-studio project in root folder
 - add CefBrowser.sln projectmap
 - remove serializationDotNet2 and re-add the project manually, add reference @ CefBrowserControl (internal project reference)
 - change your CefBrowser to x64 or x86 (depending to your needs) via configuration manager via right-click on the project-map
 - remove reference "CSharpTest.Net.RpcLibrary.dll" and add dll reference to "rpc-communication-net2\packages\CSharpTest.Net.RpcLibrary.14.327.1832.1051\lib\net20\CSharpTest.Net.RpcLibrary.dll" again
 - click rebuild on whole project map and it shoult rebuild successfully (tested on windows 10 with that steps)
 - write your code 
 - test
 - and so on...


### Why the f\*ck do I have to clone projects this way?
Cause it was the easiest way to keep sln files seperate of each other and with this way it's easier to maintain all the solutions