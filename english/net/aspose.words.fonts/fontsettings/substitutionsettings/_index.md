---
title: FontSettings.SubstitutionSettings
linktitle: SubstitutionSettings
articleTitle: SubstitutionSettings
second_title: Aspose.Words for .NET
description: Explore the FontSettings SubstitutionSettings property to optimize your font substitution process and enhance text display quality effortlessly.
type: docs
weight: 40
url: /net/aspose.words.fonts/fontsettings/substitutionsettings/
---
## FontSettings.SubstitutionSettings property

Settings related to font substitution mechanism.

```csharp
public FontSubstitutionSettings SubstitutionSettings { get; }
```

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

### See Also

* class [FontSubstitutionSettings](../../fontsubstitutionsettings/)
* class [FontSettings](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
