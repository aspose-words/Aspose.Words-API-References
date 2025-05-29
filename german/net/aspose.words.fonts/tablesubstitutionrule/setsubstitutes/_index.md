---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie Schriftnamen mit der TableSubstitutionRule SetSubstitutes-Methode anpassen. Verbessern Sie Ihr Design mit maßgeschneiderten Typografie-Lösungen!
type: docs
weight: 80
url: /de/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Ersetzen Sie die Ersatzschriftartennamen durch den angegebenen ursprünglichen Schriftnamen.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| originalFontName | String | Ursprünglicher Schriftname. |
| substituteFontNames | String[] | Liste alternativer Schriftnamen. |

## Beispiele

Zeigt, wie Regeln zum Ersetzen von Schriftarten festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Die Standardschriftartenquellen enthalten die erste Schriftart, die das Dokument verwendet.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Die zweite Schriftart „Amethysta“ ist nicht verfügbar.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Wir können eine Schriftarten-Ersetzungstabelle konfigurieren, die bestimmt
// welche Schriftarten Aspose.Words als Ersatz für nicht verfügbare Schriftarten verwenden wird.
// Legen Sie zwei Ersatzschriftarten für „Amethysta“ fest: „Arvo“ und „Courier New“.
// Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words, den zweiten Ersatz zu verwenden, und so weiter.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

    // „Amethysta“ ist nicht verfügbar und die Ersetzungsregel besagt, dass die erste als Ersatz zu verwendende Schriftart „Arvo“ ist.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

    // „Arvo“ ist ebenfalls nicht verfügbar, „Courier New“ jedoch schon.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Das Ausgabedokument zeigt den Text in der Schriftart „Amethysta“ im Format „Courier New“ an.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
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
