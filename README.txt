How to create your own AI:

Open the solution, must have .NET 4.6.1 installed

Check the project BattleCity.Common / IBattleClient.cs for interface specifications

Add your own project into the solution (SomeNewProject, project type: Class Library)

If you want to implement a WPF window, then add "Framework" references to: PresentationCore, PresentationFramework, System.Xaml, WindowsBase

Add "Solution" reference in SomeNewProject towards: BattleCity.Common

Start a new class with: "public class SomeAI : IBattleClient { }"

Right click on the text "IBattleClient" > Resolve > add "Using BattleCity.Common;"

Right click on the text "IBattleClient" > Implement interface > Implement Interface
Obligatory parts will show up. Fill them up, see BattleCity.Common / IBattleClient.cs or BattleCity._ExampleClients / AutoClient.cs for examples

Add a "Solution" reference in BattleCity.ServerGUI towards your new SomeNewProject

Build & Run > your AI should start up, shown in the GUI list (startup project: BattleCity.ServerGUI)

Select the AI modules you want to try, then click on the RUN button

In the end, you should send us the DLL and the CS file of your AI