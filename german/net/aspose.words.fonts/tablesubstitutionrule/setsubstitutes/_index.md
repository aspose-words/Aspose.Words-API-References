---
title: TableSubstitutionRule.SetSubstitutes
second_title: Aspose.Words für .NET-API-Referenz
description: TableSubstitutionRule methode. Ersetzen Sie die Namen der Ersatzschriftarten für den angegebenen Originalschriftnamen.
type: docs
weight: 80
url: /de/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Ersetzen Sie die Namen der Ersatzschriftarten für den angegebenen Originalschriftnamen.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| originalFontName | String | Ursprünglicher Schriftartname. |
| substituteFontNames | String[] | Liste alternativer Schriftartnamen. |

### Beispiele

Zeigt, wie Schriftartersetzungsregeln festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Die Standardschriftquellen enthalten die erste Schriftart, die das Dokument verwendet.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Die zweite Schriftart, „Amethysta“, ist nicht verfügbar.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Wir können eine Schriftart-Ersetzungstabelle konfigurieren, die bestimmt
// welche Schriftarten Aspose.Words als Ersatz für nicht verfügbare Schriftarten verwendet.
// Zwei Ersatzschriftarten für „Amethysta“ festlegen: „Arvo“ und „Courier New“.
// Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words, den zweiten Ersatz zu verwenden, und so weiter.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // „Amethysta“ ist nicht verfügbar und die Ersetzungsregel besagt, dass die erste Schriftart, die als Ersatz verwendet wird, „Arvo“ ist.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // „Arvo“ ist ebenfalls nicht verfügbar, „Courier New“ jedoch schon.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Das Ausgabedokument zeigt den Text an, der die Schriftart „Amethysta“ verwendet und mit „Courier New“ formatiert ist.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Zeigt, wie mit benutzerdefinierten Schriftartersetzungstabellen gearbeitet wird.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die Standard-Windows-Schriftartenersetzungstabelle.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Wenn wir Schriftarten ausschließlich aus unserem Ordner auswählen, benötigen wir eine benutzerdefinierte Ersetzungstabelle.
// Wir werden keinen Zugriff mehr auf die Microsoft Windows-Schriftarten haben,
// wie „Arial“ oder „Times New Roman“, da sie in unserem neuen Schriftartenordner nicht vorhanden sind.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Nachfolgend finden Sie zwei Möglichkeiten, eine Ersetzungstabelle aus einer Datei im lokalen Dateisystem zu laden.
// 1 - Aus einem Stream:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Direkt aus einer Datei:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Da wir keinen Zugriff mehr auf „Arial“ haben, wird unsere Schriftartentabelle zunächst versuchen, sie durch „Nicht vorhandene Schriftart“ zu ersetzen.
// Wir haben diese Schriftart nicht, sodass sie auf die nächste Ersatzschrift „Kreon“ im Ordner „MyFonts“ verschoben wird.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Wir können diese Tabelle programmgesteuert erweitern. Wir werden einen Eintrag hinzufügen, der „Times New Roman“ durch „Arvo“ ersetzt.
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Mit AddSubstitutes() können wir einen sekundären Fallback-Ersatz für einen vorhandenen Schriftarteintrag hinzufügen.
// Falls „Arvo“ nicht verfügbar ist, sucht unsere Tabelle nach „M+ 2m“ als zweite Ersatzoption.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() kann eine neue Liste von Ersatzschriftarten für eine Schriftart festlegen.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Wenn Sie Text in Schriftarten schreiben, auf die wir keinen Zugriff haben, werden unsere Ersetzungsregeln aufgerufen.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Siehe auch

* class [TableSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* Montage [Aspose.Words](../../../)


