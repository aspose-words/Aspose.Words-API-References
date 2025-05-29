---
title: SystemFontSource Class
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.SystemFontSource, Ihr Tor zum Zugriff auf alle TrueType-Schriftarten auf Ihrem System für eine nahtlose Dokumenterstellung.
type: docs
weight: 3480
url: /de/net/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class

Stellt alle im System installierten TrueType-Schriftarten dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class SystemFontSource : FontSourceBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SystemFontSource](systemfontsource/#constructor)() | Ctor. |
| [SystemFontSource](systemfontsource/#constructor_1)(*int*) | Ctor. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Gibt die Priorität der Schriftartquelle zurück. |
| override [Type](../../aspose.words.fonts/systemfontsource/type/) { get; } | Gibt den Typ der Schriftartquelle zurück. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriftarten zurück. |
| static [GetSystemFontFolders](../../aspose.words.fonts/systemfontsource/getsystemfontfolders/)() | Gibt Systemschriftordner oder ein leeres Array zurück, wenn auf die Ordner nicht zugegriffen werden kann. |

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

* class [FontSourceBase](../fontsourcebase/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
