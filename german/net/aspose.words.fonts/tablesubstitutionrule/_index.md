---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
articleTitle: TableSubstitutionRule
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.TableSubstitutionRule für effiziente Schriftartverwaltung und nahtlose Textformatierung in Ihren Dokumenten.
type: docs
weight: 3490
url: /de/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Regel zur Ersetzung von Tabellenschriftarten.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Gibt an, ob die Regel aktiviert ist oder nicht. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(*string, params string[]*) | Fügt Ersatzschriftartennamen für den angegebenen ursprünglichen Schriftnamen hinzu. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(*string*) | Gibt ein Array zurück, das Ersatzschriftnamen für den angegebenen ursprünglichen Schriftnamen enthält. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(*Stream*) | Lädt Tabellensubstitutionseinstellungen aus dem XML-Stream. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(*string*) | Lädt Tabellensubstitutionseinstellungen aus einer XML-Datei. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Lädt vordefinierte Tabellenersetzungseinstellungen für die Android-Plattform. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Lädt vordefinierte Tabellensubstitutionseinstellungen für die Linux-Plattform. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Lädt vordefinierte Tabellensubstitutionseinstellungen für die Windows-Plattform. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(*Stream*) | Speichert die aktuellen Tabellensubstitutionseinstellungen im Stream. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(*string*) | Speichert die aktuellen Tabellenersetzungseinstellungen in einer Datei. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(*string, params string[]*) | Ersetzen Sie die Ersatzschriftartennamen durch den angegebenen ursprünglichen Schriftnamen. |

## Bemerkungen

Diese Regel definiert die Liste der Ersatzschriftarten, die verwendet werden sollen, wenn die Originalschriftart nicht verfügbar ist. Ersatzschriften werden auf den Schriftnamen und die[`AltName`](../fontinfo/altname/) (falls vorhanden).

## Beispiele

Zeigt, wie auf Schriftartenersetzungstabellen für Windows und Linux zugegriffen wird.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die standardmäßige Schriftartersetzungstabelle von Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// Unter Windows ist „Times New Roman“ der Standardersatz für die Schriftart „Times New Roman CE“.
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Wir können die Tabelle in Form eines XML-Dokuments speichern.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux hat eine eigene Substitutionstabelle.
// Es gibt mehrere Ersatzschriften für „Times New Roman CE“.
// Wenn der erste Ersatz, „FreeSerif“, auch nicht verfügbar ist,
// Diese Regel durchläuft die anderen im Array, bis sie eine verfügbare findet.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Speichern Sie die Linux-Substitutionstabelle mithilfe eines Streams in Form eines XML-Dokuments.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Siehe auch

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
