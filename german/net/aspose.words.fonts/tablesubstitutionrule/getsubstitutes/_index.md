---
title: TableSubstitutionRule.GetSubstitutes
linktitle: GetSubstitutes
articleTitle: GetSubstitutes
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetSubstitutes-Methode in TableSubstitutionRule. Rufen Sie ganz einfach Ersatzschriftarten für Ihre Originalschriftart ab und erhöhen Sie so die Designflexibilität.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/tablesubstitutionrule/getsubstitutes/
---
## TableSubstitutionRule.GetSubstitutes method

Gibt ein Array zurück, das Ersatzschriftnamen für den angegebenen ursprünglichen Schriftnamen enthält.

```csharp
public IEnumerable<string> GetSubstitutes(string originalFontName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| originalFontName | String | Ursprünglicher Schriftname. |

### Rückgabewert

Liste alternativer Schriftnamen.

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

Zeigt, wie mit benutzerdefinierten Schriftartersetzungstabellen gearbeitet wird.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die standardmäßige Windows-Schriftartenersetzungstabelle.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Wenn wir Schriftarten ausschließlich aus unserem Ordner auswählen, benötigen wir eine benutzerdefinierte Ersetzungstabelle.
// Wir haben keinen Zugriff mehr auf die Microsoft Windows-Schriftarten,
// wie „Arial“ oder „Times New Roman“, da diese in unserem neuen Schriftartenordner nicht vorhanden sind.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Unten sind zwei Möglichkeiten zum Laden einer Substitutionstabelle aus einer Datei im lokalen Dateisystem aufgeführt.
// 1 - Aus einem Stream:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Direkt aus einer Datei:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Da wir keinen Zugriff mehr auf „Arial“ haben, versucht unsere Schriftartentabelle zunächst, es durch „Nicht vorhandene Schriftart“ zu ersetzen.
// Wir haben diese Schriftart nicht, daher wechseln wir zum nächsten Ersatz, „Kreon“, der sich im Ordner „MyFonts“ befindet.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Wir können diese Tabelle programmgesteuert erweitern. Wir fügen einen Eintrag hinzu, der "Times New Roman" durch "Arvo" ersetzt.
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Mit AddSubstitutes() können wir einen sekundären Fallback-Ersatz für einen vorhandenen Schriftarteintrag hinzufügen.
// Falls „Arvo“ nicht verfügbar ist, sucht unsere Tabelle nach „M+ 2m“ als zweite Ersatzoption.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() kann eine neue Liste mit Ersatzschriftarten für eine Schriftart festlegen.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Wenn wir Text in Schriftarten schreiben, auf die wir keinen Zugriff haben, werden unsere Ersetzungsregeln aufgerufen.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Siehe auch

* class [TableSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
