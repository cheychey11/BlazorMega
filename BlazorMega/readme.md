# BlazorMega Component Library

A reusable Blazor component library for .NET 9 with modern, customizable UI components.

## ?? Installation

Install the package via NuGet:

```bash
dotnet add package BlazorMega
```

Or via the Package Manager Console:

```powershell
Install-Package BlazorMega
```

## ?? Getting Started

### 1. Add the namespace

Add the following to your `_Imports.razor`:

```razor
@using BlazorMega.Components
```

### 2. Include the CSS

Add the component styles to your `App.razor` or main layout:

```html
<link rel="stylesheet" href="_content/BlazorMega/BlazorMega.bundle.scp.css" />
```

### 3. Use the components

Start using components in your Blazor pages:

```razor
<MyButton OnClick="HandleClick">Click Me!</MyButton>
```

## ?? Components

### MyButton

A customizable button component with icon support and smooth animations.

#### Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `ChildContent` | `RenderFragment?` | - | The content displayed inside the button |
| `Icon` | `string?` | `null` | Optional icon or emoji to display before the text |
| `CssClass` | `string` | `""` | Additional CSS classes to apply |
| `Type` | `string` | `"button"` | The HTML button type attribute |
| `Disabled` | `bool` | `false` | Whether the button is disabled |
| `OnClick` | `EventCallback<MouseEventArgs>` | - | Event handler for button clicks |

#### Examples

**Basic Button:**
```razor
<MyButton OnClick="@(() => Console.WriteLine("Clicked!"))">
    Click Me
</MyButton>
```

**Button with Icon:**
```razor
<MyButton Icon="??" OnClick="LaunchRocket">
    Launch
</MyButton>
```

**Disabled Button:**
```razor
<MyButton Disabled="true">
    Cannot Click
</MyButton>
```

**Custom Styled Button:**
```razor
<MyButton CssClass="my-custom-class" Icon="?" OnClick="SaveData">
    Save Changes
</MyButton>
```

**Submit Button:**
```razor
<MyButton Type="submit" OnClick="HandleSubmit">
    Submit Form
</MyButton>
```

## ?? Styling

The `MyButton` component comes with built-in styles that include:
- Smooth hover effects with elevation
- Active state animations
- Disabled state styling
- Flexbox layout for icon alignment

You can override or extend these styles by:
1. Adding custom CSS classes via the `CssClass` parameter
2. Using CSS specificity to override the default `.btn-mega` styles
3. Creating your own theme by targeting the component's CSS classes

## ??? Development

### Building the Library

To build the library locally:

```bash
dotnet build
```

### Creating a NuGet Package

To create a NuGet package:

```bash
dotnet pack --configuration Release
```

The `.nupkg` file will be generated in `bin/Release/`.

### Publishing to NuGet

```bash
dotnet nuget push bin/Release/BlazorMega.1.0.0.nupkg --api-key YOUR_API_KEY --source https://api.nuget.org/v3/index.json
```

## ?? Requirements

- **.NET 9.0** or later
- Compatible with:
  - Blazor Server
  - Blazor WebAssembly
  - Blazor Auto render mode

## ??? Roadmap

Future components planned:
- Card component
- Modal/Dialog component
- Input components with validation
- Navigation components
- Data grid component

## ?? License

This project is licensed under the MIT License.

## ?? Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingComponent`)
3. Commit your changes (`git commit -m 'Add AmazingComponent'`)
4. Push to the branch (`git push origin feature/AmazingComponent`)
5. Open a Pull Request

Please ensure your code:
- Follows .NET coding conventions
- Includes XML documentation comments
- Works with all Blazor render modes
- Includes examples in the README

## ?? Links

- **Repository**: [github.com/cheychey11/BlazorMega](https://github.com/cheychey11/BlazorMega)
- **Issues**: [Report a bug or request a feature](https://github.com/cheychey11/BlazorMega/issues)
- **NuGet Package**: Coming soon!

## ?? Support

If you have questions or need help:
- Open an issue on GitHub
- Check existing issues for solutions
- Review the examples in this README

---

Made with ?? for the Blazor community
