# Radzen.Blazor.Sample
Radzen Controls Blazor Integration

## Get started with the Radzen Blazor Components

### Install

Radzen Blazor Components are distributed as the Radzen.Blazor nuget package. You can add them to your project in one of the following ways
- Install the package from command line by running dotnet add package Radzen.Blazor
- Add the project from the Visual Nuget Package Manager 
- Manually edit the .csproj file and add a project reference

### Import the namespace

Open the `_Imports.razor` file of your Blazor application and add this line `@using Radzen.Blazor`.

### Include a theme

Open the `_Host.cshtml` file (server-side Blazor) or `wwwroot/index.html` (client-side Blazor) and include a theme CSS file by adding this snippet `<link rel="stylesheet" href="_content/Radzen.Blazor/css/default.css">` or `<link rel="stylesheet" href="_content/Radzen.Blazor/css/default-base.css">` if you either include Bootstrap manually or don't use it at all.

### Include Radzen.Blazor.js

Open the `_Host.cshtml` file (server-side Blazor) or `wwwroot/index.html` (client-side Blazor) and include this snippet `<script src="_content/Radzen.Blazor/Radzen.Blazor.js"></script>`

### Use a component
Use any Radzen Blazor component by typing its tag name in a Blazor page e.g. 
```html
<RadzenButton Text="Hi"></RadzenButton>
```

#### Data-binding a property
```razor
<RadzenButton Text=@text />
<RadzenTextBox @bind-Value=@text />
@code {
  string text = "Hi";
}
```

#### Handing events

```razor
<RadzenButton Click="@ButtonClicked" Text="Hi"></RadzenButton>
@code {
  void ButtonClicked()
  {

  }
}
```
