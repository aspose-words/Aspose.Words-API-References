---
title: FontSubstitutionSettings Class
linktitle: FontSubstitutionSettings
articleTitle: FontSubstitutionSettings
second_title: Aspose.Words für .NET
description: Aspose.Words.Fonts.FontSubstitutionSettings klas. Gibt die Einstellungen für den Schriftartersetzungsmechanismus an in C#.
type: docs
weight: 3010
url: /de/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Gibt die Einstellungen für den Schriftartersetzungsmechanismus an.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class FontSubstitutionSettings
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Einstellungen im Zusammenhang mit der Standardregel zum Ersetzen von Schriftarten. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Einstellungen im Zusammenhang mit der Ersetzungsregel für die Schriftartkonfiguration. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Einstellungen im Zusammenhang mit der Regel zum Ersetzen von Schriftartinformationen. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Einstellungen im Zusammenhang mit der Regel zum Ersetzen von Schriftartnamen. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Einstellungen im Zusammenhang mit der Tabellenersetzungsregel. |

## Bemerkungen

Der Schriftersetzungsprozess besteht aus mehreren Regeln, die nacheinander in einer bestimmten Reihenfolge überprüft werden. Wenn die erste Regel die Schriftart nicht auflösen kann, wird die zweite Regel überprüft und so weiter.

Die Reihenfolge der Regeln ist wie folgt: 1. Regel zum Ersetzen von Schriftartnamen (standardmäßig aktiviert) 2. Regel zum Ersetzen von Schriftartenkonfiguration (standardmäßig deaktiviert) 3. Regel zum Ersetzen von Tabellen (standardmäßig aktiviert) 4. Regel zum Ersetzen von Schriftartinformationen (standardmäßig aktiviert) 5. Standardschriftartregel (standardmäßig aktiviert)

Beachten Sie, dass die Schriftart-Info-Ersetzungsregel die Schriftart immer auflöst, wenn[`FontInfo`](../fontinfo/) ist verfügbar und überschreibt die Standardschriftartregel. Wenn Sie die Standard-Schriftartenregel verwenden möchten, sollten Sie die Schriftinformations-Ersetzungsregel deaktivieren.

Beachten Sie, dass die Schriftart-Konfigurationsersetzungsregel in den meisten Fällen die Schriftart auflöst und somit alle anderen Regeln außer Kraft setzt.

## Beispiele

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

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
