---
title: SystemFontSource.GetSystemFontFolders
second_title: Aspose.Words für .NET-API-Referenz
description: SystemFontSource methode. Gibt Systemschriftartenordner oder ein leeres Array zurück wenn auf Ordner nicht zugegriffen werden kann.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/systemfontsource/getsystemfontfolders/
---
## SystemFontSource.GetSystemFontFolders method

Gibt Systemschriftartenordner oder ein leeres Array zurück, wenn auf Ordner nicht zugegriffen werden kann.

```csharp
public static string[] GetSystemFontFolders()
```

### Bemerkungen

Auf einigen Plattformen konnte Aspose.Words Systemschriftarten nicht nur in Ordnern, sondern auch in anderen Quellen durchsuchen. Beispielsweise suchen Aspose.Words auf der Windows-Plattform Schriftarten auch in der Registrierung.

### Beispiele

Zeigt, wie Sie auf die Systemschriftquelle eines Dokuments zugreifen und Schriftartersatz festlegen.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Standardmäßig enthält ein leeres Dokument immer eine Systemschriftquelle.
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

// Legen Sie eine Schriftart fest, die im Windows-Schriftartenverzeichnis vorhanden ist, als Ersatz für eine Schriftart, die nicht vorhanden ist.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternativ könnten wir einen Ordner „Font Source“ hinzufügen, in dem der entsprechende Ordner die Schriftart enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Durch das Zurücksetzen der Schriftartenquellen verbleiben weiterhin die Systemschriftquelle sowie unsere Ersatzschriftarten.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### Siehe auch

* class [SystemFontSource](../)
* namensraum [Aspose.Words.Fonts](../../systemfontsource/)
* Montage [Aspose.Words](../../../)


