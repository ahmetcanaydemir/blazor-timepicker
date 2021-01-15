# Blazor Time Picker

This component provides a 24H dropdown time picker in blazor with bindings. It is closing when you click outside. You can change time directly via input text. Also you can use arrow keys, mouse wheel or icons to change hour or minute.

![Blazor Time Picker Sample](/assets/sample.png)

You can use it directly with a timespan.

```html
<TimePicker @bind-Time="@TimeSpan" />
```

Also you have other bindings. Full example:

```csharp
<ul>
    <li>Timespan = @TimeSpan.Hours, @TimeSpan.Minutes</li>
    <li>Hours = @Hours</li>
    <li>Minutes = @Minutes</li>
    <li>Input Text = @TextValue</li>
</ul>

<TimePicker
             @bind-Time="@TimeSpan"
             @bind-Minute="@Minutes"
             @bind-Hour="@Hours"
             @bind-Value="@TextValue"
             @bind-TimePickerVisible="@Visible"
             />

@code{
    public TimeSpan TimeSpan { get; set; } = new TimeSpan(12, 45, 0);
    public int Minutes { get; set; }
    public int Hours { get; set; }
    public string TextValue { get; set; }
    public bool Visible { get; set; }
}
```

## Setup

This component using Bootstrap 4's CSS so you need to add if you don't have already in your project.

1. Add this project to your project dependencies. (I will create nuget package later.)

2. Add this css to \_Host.cshtml:

```html
<link href="_content/blazor_timepicker/index.css" rel="stylesheet" />
```

3. Add this script to \_Host.cshtml:

```html
<script src="_content/blazor_timepicker/index.js"></script>
```

## Licensing

Licensed under the [MIT](/LICENSE).
