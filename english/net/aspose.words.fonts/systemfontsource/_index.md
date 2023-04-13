---
title: SystemFontSource Class
linktitle: SystemFontSource
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Fonts.SystemFontSource class. Represents all TrueType fonts installed to the system in C#.
type: docs
weight: 2930
url: /net/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class

Represents all TrueType fonts installed to the system.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class SystemFontSource : FontSourceBase
```

## Constructors

| Name | Description |
| --- | --- |
| [SystemFontSource](systemfontsource/#constructor)() | Ctor. |
| [SystemFontSource](systemfontsource/#constructor_1)(int) | Ctor. |

## Properties

| Name | Description |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returns the font source priority. |
| override [Type](../../aspose.words.fonts/systemfontsource/type/) { get; } | Returns the type of the font source. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |
| static [GetSystemFontFolders](../../aspose.words.fonts/systemfontsource/getsystemfontfolders/)() | Returns system font folders or empty array if folders are not accessible. |

## Examples

Shows how to access a document's system font source and set font substitutes.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// By default, a blank document always contains a system font source.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternatively, we could add a folder font source in which the corresponding folder contains the font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Resetting the font sources still leaves us with the system font source as well as our substitutes.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### See Also

* class [FontSourceBase](../fontsourcebase/)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
