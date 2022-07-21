---
title: SetSubstitutes
second_title: Aspose.Words für .NET-API-Referenz
description: Ersatzschriftnamen für den angegebenen Originalschriftnamen überschreiben.
type: docs
weight: 80
url: /de/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Ersatzschriftnamen für den angegebenen Originalschriftnamen überschreiben.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| originalFontName | String | Name der ursprünglichen Schriftart. |
| substituteFontNames | String[] | Liste alternativer Schriftnamen. |

### Beispiele

Zeigt, wie Schriftersetzungsregeln festgelegt werden.

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

// Die zweite Schriftart, "Amethysta", ist nicht verfügbar.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Wir können eine Font-Ersetzungstabelle konfigurieren, die bestimmt
// welche Schriftarten Aspose.Words als Ersatz für nicht verfügbare Schriftarten verwendet.
// Legen Sie zwei Ersatzschriftarten für "Amethysta" fest: "Arvo" und "Courier New".
// Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words, den zweiten Ersatz zu verwenden, und so weiter.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" ist nicht verfügbar, und die Ersetzungsregel besagt, dass die erste als Ersatz zu verwendende Schriftart "Arvo" ist.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // „Arvo“ ist ebenfalls nicht verfügbar, „Courier New“ hingegen schon.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Das Ausgabedokument zeigt den Text mit der Schriftart "Amethysta" formatiert mit "Courier New" an.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
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
