---
title: AddSubstitutes
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt Ersatzschriftnamen für den angegebenen Originalschriftnamen hinzu.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/tablesubstitutionrule/addsubstitutes/
---
## TableSubstitutionRule.AddSubstitutes method

Fügt Ersatzschriftnamen für den angegebenen Originalschriftnamen hinzu.

```csharp
public void AddSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| originalFontName | String | Name der ursprünglichen Schriftart. |
| substituteFontNames | String[] | Liste alternativer Schriftnamen. |

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

// Festlegen einer im Windows Fonts-Verzeichnis vorhandenen Schriftart als Ersatz für eine nicht vorhandene Schriftart.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternativ könnten wir einen Ordner font source hinzufügen, in dem der entsprechende Ordner die Schriftart enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Das Zurücksetzen der Schriftartquellen lässt uns immer noch die Systemschriftquelle sowie unsere Ersatzquellen.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

Zeigt, wie Sie mit benutzerdefinierten Zeichensatzersetzungstabellen arbeiten.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die standardmäßige Windows-Zeichensatzersetzungstabelle.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Wenn wir Schriftarten ausschließlich aus unserem Ordner auswählen, benötigen wir eine benutzerdefinierte Substitutionstabelle.
// Wir haben keinen Zugriff mehr auf die Microsoft Windows-Schriftarten,
// wie "Arial" oder "Times New Roman", da sie in unserem neuen Schriftartenordner nicht vorhanden sind.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Im Folgenden finden Sie zwei Möglichkeiten, eine Substitutionstabelle aus einer Datei im lokalen Dateisystem zu laden.
// 1 - Aus einem Stream:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Direkt aus einer Datei:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Da wir keinen Zugriff mehr auf "Arial" haben, versucht unsere Font-Tabelle zuerst, sie durch "Nonexistent Font" zu ersetzen.
// Wir haben diese Schriftart nicht, sodass sie zum nächsten Ersatz "Kreon" verschoben wird, der sich im Ordner "MyFonts" befindet.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Wir können diese Tabelle programmgesteuert erweitern. Wir werden einen Eintrag hinzufügen, der „Times New Roman“ durch „Arvo“ ersetzt.
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Mit AddSubstitutes() können wir einen sekundären Fallback-Ersatz für einen bestehenden Font-Eintrag hinzufügen.
// Falls "Arvo" nicht verfügbar ist, sucht unsere Tabelle nach "M+ 2m" als zweite Ersatzoption.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() kann eine neue Liste von Ersatzfonts für einen Font setzen.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Das Schreiben von Text in Schriftarten, auf die wir keinen Zugriff haben, ruft unsere Ersetzungsregeln auf.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Siehe auch

* class [TableSubstitutionRule](../../tablesubstitutionrule)
* namensraum [Aspose.Words.Fonts](../../tablesubstitutionrule)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
