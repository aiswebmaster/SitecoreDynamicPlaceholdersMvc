[![NuGet](https://img.shields.io/nuget/v/SitecoreMaster.TrueDynamicPlaceholders.svg)]() [![NuGet](https://img.shields.io/nuget/dt/SitecoreMaster.TrueDynamicPlaceholders.svg)]()

# Sitecore Dynamic Placeholders for Mvc

This module allows you to build complex Sitecore sites with the use of Dynamic Placeholders.  This project is built using Helix best practices and currently exists on the Sitecore Marketplace: 

## What makes this Dynamic Placeholder module different?

There are alot of Dynamic Placeholders modules currently available for Sitecore, but this one is different because even though it supports truly dynamic placeholders, it also doesn't completely clutter the Rendering Details for your page, like other Dynamic Placeholder modules do.  Most are based on using a unique identifier, such as an incrementing id or the rendering id.  Creating a new presentation detail with that approach, is fairly straight forward, especially with the incrementing number approach.  The problem however surfaces when you try to reorder your renderings or remove existing renderings.  Now you have to calculate how to use the correct incrementing id to get your renderings to display.

This dynamic placeholder logic however doesn't rely on any additional increments or unique identifiers to the placeholder name.  Instead it uses the order that the renderings sit in the presentation details to determine where they should be placed.  So re-orderings a collection of renderings is straight forward, because you only need to move them around in the presentation details.

# Installation

1. Download the latest Sitecore package below from the Sitecore marketplace here and install like you would with any other module (or using the Sitecore Instance Manager).

   <https://marketplace.sitecore.net/en/Modules/T/True_Dynamic_Placeholders.aspx>

2. In your project/solution, use NuGet to pull in the required references, so that you can use the helper methods within your views.

```csharp
Install-Package SitecoreMaster.TrueDynamicPlaceholders -Version 1.0.4
```

3. Define areas of your page to use the Dynamic Placeholders by using the unique html helper:

```csharp
@Html.Sitecore().TrueDynamicPlaceholder("Key");
```

That's it, once you have placed the Dynamic Placeholder helper, you can start placing renderings using the hierarchy that makes sense for your project.

We recommend that you only use the Dynamic Placeholder, rather than mixing the traditional Sitecore placeholder with the 'Dynamic Placeholder' logic.

This has been tested with Sitecore 8.0+

