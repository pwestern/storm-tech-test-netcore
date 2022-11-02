# Storm Technical Test – A Todo-List Project

This is a todo-list webapp written in C# using [.NET 6.0](https://get.asp.net).

Show us what you've got by knocking it into shape!

## Requirements
- [.NET 6](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- [EF Core tools](https://learn.microsoft.com/en-us/ef/core/cli/dotnet)

## Practicalities

Please make a fork of this project for your work.

Each commit you make should relate to a single task. A more complex task may have many commits; this is up to you.

The app runs on Windows, macOS, and Linux. It can be built using Visual Studio 2019, Visual Studio Code, or command line. On the command line: 

| What | How |
|-|-|
| create database | `dotnet ef database update` |
| build | `dotnet build` |
| run unit tests | `dotnet test Todo.Tests` |
| run | `dotnet run --project Todo` |

If you run the tests, you should see that one fails. This is deliberate.

## The app

The app allows a user to create multiple todo-lists. Each list has a number of items. Each item has an importance and a person responsible for completion.

## Tasks

Tasks are in ascending order of difficulty. Complete as many, or as few, tasks that you feel able to. Add unit tests if you can.

> **Hey this is important!**
> We hope you can spend between 3 and 5 hours on this project. If you can finish faster -- great! If not, limit yourself and don't spend much longer than 5 hours MAX.

If you want to document any aspects of your solution, please use `SOLUTION.md` in the root of the repository.

| # | Description |
|-|-|
| 1 | Build and run the app. Register a user account, make some lists, add some items – have a play and get familiar with the app. |
| 2 | When todo items are displayed in browser in the details page, they are listed in an arbitrary order. Change `Views/TodoList/Detail.cshtml` so that items are listed by order of importance: `High`, `Medium`, `Low` |
| 3 | Run the unit tests. One test should be failing. The process that maps a `TodoItem` to a `TodoItemEditFields` instance is failing - the `Importance` field is not copied. Fix the bug and ensure the test passes. |
| 4 | Make it so that the edit and create item pages show friendly text instead of "ResponsiblePartyId"  |
| 5 | On the details page, add an option to hide items that are marked as done. |
| 6 | Currently `/TodoList` shows all todo-lists that the user is owner of. Change this so it also shows todo-lists that the user has at least one item where they are marked as the responsible party  |
| 7 | Add a `Rank` property to the `TodoItem` class. Add an EntityFramework migration to reflect this change. Allow a user to set the rank property on the edit page. Add a new option on the details page to order by rank. |
| 8 | If the users you register have an avatar added to gravatar.com, then you will see that avatar by their email address in the navigation area and beside items in a list. Instead of just showing an email address to identify a user, make an enhancement that uses the gravatar.com API to download profile information (if any), and extract the user's name. Display the name along side the email address. Consider what would happen if the gravatar service was slow to respond or not working. |
| 9 | The process of adding items to a list is pretty clunky; the user has to go to a new page, fill in a form, then go back to the list detail page. It would be easier for the user to do all that on the list detail page. Replace the "Add New Item" link with UI that allows creation of items without navigating away from the detail page. You will need to use Javascript and an API that you create. |
| 10 | Add an API that allows setting of the `Rank` property (added in Task 8). Add Javascript functionality that allows reordering of list items by rank without navigating away from the detail page |
