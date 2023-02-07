---
title: TableSubstitutionRule.Load
second_title: Aspose.Words for .NET API Reference
description: Loads table substitution settings from XML file in C#
type: docs
weight: 30
url: /net/aspose.words.fonts/tablesubstitutionrule/load/
---
## Load(string) {#load_1}

Loads table substitution settings from XML file.

```csharp
public void Load(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Input file name. |

## Examples

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

---

## Load(Stream) {#load}

Loads table substitution settings from XML stream.

```csharp
public void Load(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Input stream. |

## Examples

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
