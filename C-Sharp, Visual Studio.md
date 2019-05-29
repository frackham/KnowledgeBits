## C# / Visual Studio

### C#

#### C# Testing
Autofixture <-- generate test data as well as autopop mocks?
Moq.

### Visual Studio


c#
https://www.automatetheplanet.com/applications/most-complete-nunit-cheat-sheet/
This only works if the object is fully serializable.
(new System.Xml.Serialization.XmlSerializer(obj.GetType())).Serialize(new System.IO.StreamWriter(@"c:\temp\text.xml"), obj)
Alternative for the immediate window (only if < 100 lines) …(else try the watch window)
?variableName
Test regexes for c#:
http://regexstorm.net/tester
https://yoda.entelect.co.za/view/4359/setup-your-vs-project-to-transform-your-web-config-on-build
https://deanhume.com/working-with-multiple-web-config-files/
https://stackoverflow.com/questions/4454016/multiple-app-config-files-in-net-class-library-project <-- note what is said about configuration manager…always from default.
@ThePracticalDev: A few things to look out for when using TransactionScope include:
- Handling Multiple Connections Across Different Databases
- Handling Asynchronous (e.g. async/await)
- Timeout-related Errors
{ author: @rionmonster } #DEVCommunity https://dev.to/rionmonster/slightly-rough-exchanges-troubleshooting-transactional-issues-with-transactionscope-2494
Shared via TweetCaster
https://www.codeproject.com/Articles/18698/Log-Error-and-Information-Messages-in-Two-Differen
https://stackoverflow.com/questions/8926409/log4net-hierarchy-and-logging-levels
https://www.kruegerwebdesign.com/2015/06/22/how-to-use-the-log4net-stringmatchfilter/
Subject: Log4net Tutorial for .NET Logging: 14 Best Practices and Examples
https://www.google.com/amp/s/stackify.com/log4net-guide-dotnet-logging/amp/
surround error line with try catch
1.         Select code in question.
2.         CTRL+K
3.         CTRL+S  brings up snippets manager thing
4.         ‘try’ and enter
5.         :)
@dotnetkicks: Using Stopwatch and ContinueWith to Measure Task Execution Time in C# by ExceptionFound https://dotnetkicks.com/r/390344?url=https://exceptionnotfound.net/using-stopwatch-and-continuewith-to-measure-task-execution-time-in-c/ #dotnet via DotNetKicks
Shared via TweetCaster
https://stackoverflow.com/questions/3802027/how-do-i-programmatically-list-all-projects-in-a-solution
https://refactoring.guru/replace-conditional-with-polymorphism
