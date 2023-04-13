---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Fonts.TableSubstitutionRule class. Table font substitution rule in C#.
type: docs
weight: 2940
url: /net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Table font substitution rule.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## Properties

| Name | Description |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Specifies whether the rule is enabled or not. |

## Methods

| Name | Description |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(string, params string[]) | Adds substitute font names for given original font name. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(string) | Returns array containing substitute font names for the specified original font name. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(Stream) | Loads table substitution settings from XML stream. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(string) | Loads table substitution settings from XML file. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Loads predefined table substitution settings for Android platform. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Loads predefined table substitution settings for Linux platform. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Loads predefined table substitution settings for Windows platform. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(Stream) | Saves the current table substitution settings to stream. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(string) | Saves the current table substitution settings to file. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(string, params string[]) | Override substitute font names for given original font name. |

## Remarks

This rule defines the list of substitute font names to be used if the original font is not available. Substitutes will be checked for the font name and the [`AltName`](../fontinfo/altname/) (if any).

## Examples

Shows how to access font substitution tables for Windows and Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Create a new table substitution rule and load the default Microsoft Windows font substitution table.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// We can save the table in the form of an XML document.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux has its own substitution table.
// There are multiple substitute fonts for "Times New Roman CE".
// If the first substitute, "FreeSerif" is also unavailable,
// this rule will cycle through the others in the array until it finds an available one.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Save the Linux substitution table in the form of an XML document using a stream.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### See Also

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
