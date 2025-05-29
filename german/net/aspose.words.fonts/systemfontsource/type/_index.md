---
title: SystemFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „SystemFontSource Type“, greifen Sie einfach auf Schriftartquellentypen zu und identifizieren Sie sie, um Ihr Webdesign und die Benutzererfahrung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/systemfontsource/type/
---
## SystemFontSource.Type property

Gibt den Typ der Schriftartquelle zurück.

```csharp
public override FontSourceType Type { get; }
```

## Beispiele

Zeigt, wie Sie auf die Systemschriftartquelle eines Dokuments zugreifen und Schriftartenersatz festlegen.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Standardmäßig enthält ein leeres Dokument immer eine Systemschriftartquelle.
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

// Legen Sie eine Schriftart fest, die im Windows-Schriftartenverzeichnis als Ersatz für eine Schriftart vorhanden ist, die dort nicht vorhanden ist.
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

// Durch das Zurücksetzen der Schriftartquellen bleiben uns weiterhin die Systemschriftartquelle und unsere Ersatzschriften erhalten.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
```

### Siehe auch

* enum [FontSourceType](../../fontsourcetype/)
* class [SystemFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
