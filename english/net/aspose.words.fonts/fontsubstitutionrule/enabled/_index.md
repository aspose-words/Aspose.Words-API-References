---
title: FontSubstitutionRule.Enabled
linktitle: Enabled
articleTitle: Enabled
second_title: Aspose.Words for .NET
description: Discover the FontSubstitutionRule Enabled property to easily manage font settings. Ensure optimal text display with this essential feature.
type: docs
weight: 10
url: /net/aspose.words.fonts/fontsubstitutionrule/enabled/
---
## FontSubstitutionRule.Enabled property

Specifies whether the rule is enabled or not.

```csharp
public virtual bool Enabled { get; set; }
```

## Examples

Shows operating system-dependent font config substitution.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
// On Windows, it is unavailable.
if (isWindows)
{
    Assert.That(fontConfigSubstitution.Enabled, Is.False);
    Assert.That(fontConfigSubstitution.IsFontConfigAvailable(), Is.False);
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// On Linux/Mac, we will have access to it, and will be able to perform operations.
if (isLinuxOrMac)
{
    Assert.That(fontConfigSubstitution.Enabled, Is.True);
    Assert.That(fontConfigSubstitution.IsFontConfigAvailable(), Is.True);

    fontConfigSubstitution.ResetCache();
}
```

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

* class [FontSubstitutionRule](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
