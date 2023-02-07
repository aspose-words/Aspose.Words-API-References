---
title: TableSubstitutionRule.SetSubstitutes
second_title: Aspose.Words for .NET API Reference
description: TableSubstitutionRule method. Override substitute font names for given original font name in C#
type: docs
weight: 80
url: /net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Override substitute font names for given original font name.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | String | Original font name. |
| substituteFontNames | String[] | List of alternative font names. |

## Examples

Shows how set font substitution rules.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// The default font sources contain the first font that the document uses.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// The second font, "Amethysta", is unavailable.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// We can configure a font substitution table which determines
// which fonts Aspose.Words will use as substitutes for unavailable fonts.
// Set two substitution fonts for "Amethysta": "Arvo", and "Courier New".
// If the first substitute is unavailable, Aspose.Words attempts to use the second substitute, and so on.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

// "Amethysta" is unavailable, and the substitution rule states that the first font to use as a substitute is "Arvo". 
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// "Arvo" is also unavailable, but "Courier New" is. 
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// The output document will display the text that uses the "Amethysta" font formatted with "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Shows how to work with custom font substitution tables.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Create a new table substitution rule and load the default Windows font substitution table.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// If we select fonts exclusively from our folder, we will need a custom substitution table.
// We will no longer have access to the Microsoft Windows fonts,
// such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Below are two ways of loading a substitution table from a file in the local file system.
// 1 -  From a stream:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 -  Directly from a file:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
// We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
// In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() can set a new list of substitute fonts for a font.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Writing text in fonts that we do not have access to will invoke our substitution rules.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### See Also

* class [TableSubstitutionRule](../)
* namespace [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
