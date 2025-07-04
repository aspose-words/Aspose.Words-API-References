---
title: TableSubstitutionRule.AddSubstitutes
linktitle: AddSubstitutes
articleTitle: AddSubstitutes
second_title: Aspose.Words for .NET
description: Enhance your typography with the TableSubstitutionRule AddSubstitutes method, allowing seamless integration of substitute fonts for any original font.
type: docs
weight: 10
url: /net/aspose.words.fonts/tablesubstitutionrule/addsubstitutes/
---
## TableSubstitutionRule.AddSubstitutes method

Adds substitute font names for given original font name.

```csharp
public void AddSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | String | Original font name. |
| substituteFontNames | String[] | List of alternative font names. |

## Examples

Shows how to access a document's system font source and set font substitutes.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// By default, a blank document always contains a system font source.
Assert.That(doc.FontSettings.GetFontsSources().Length, Is.EqualTo(1));

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.That(systemFontSource.Type, Is.EqualTo(FontSourceType.SystemFonts));
Assert.That(systemFontSource.Priority, Is.EqualTo(0));

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.That(SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower(), Is.EqualTo(fontsPath.ToLower()));
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.That(doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count(), Is.EqualTo(1));
Assert.That(doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray(), Does.Contain("Calibri"));

// Alternatively, we could add a folder font source in which the corresponding folder contains the font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.That(doc.FontSettings.GetFontsSources().Length, Is.EqualTo(2));

// Resetting the font sources still leaves us with the system font source as well as our substitutes.
doc.FontSettings.ResetFontSources();

Assert.That(doc.FontSettings.GetFontsSources().Length, Is.EqualTo(1));
Assert.That(doc.FontSettings.GetFontsSources()[0].Type, Is.EqualTo(FontSourceType.SystemFonts));
Assert.That(doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count(), Is.EqualTo(1));
Assert.That(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled, Is.True);
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
Assert.That(tableSubstitutionRule.GetSubstitutes("Arial").ToArray(), Is.EqualTo(new[] {"Missing Font", "Kreon"}));

// We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
Assert.That(tableSubstitutionRule.GetSubstitutes("Times New Roman"), Is.Null);
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.That(tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray(), Is.EqualTo(new[] {"Arvo"}));

// We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
// In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.That(tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray(), Is.EqualTo(new[] {"Arvo", "M+ 2m"}));

// SetSubstitutes() can set a new list of substitute fonts for a font.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.That(tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray(), Is.EqualTo(new[] {"Squarish Sans CT", "M+ 2m"}));

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
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
