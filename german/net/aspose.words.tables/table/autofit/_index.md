---
title: Table.AutoFit
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Ändert die Größe der Tabelle und der Zellen entsprechend dem angegebenen automatischen Anpassungsverhalten.
type: docs
weight: 380
url: /de/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Ändert die Größe der Tabelle und der Zellen entsprechend dem angegebenen automatischen Anpassungsverhalten.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| behavior | AutoFitBehavior | Gibt an, wie die Tabelle automatisch angepasst wird. |

### Bemerkungen

Diese Methode ahmt die Befehle nach, die im Menü „Automatisch anpassen“ für eine Tabelle in Microsoft Word verfügbar sind. Die verfügbaren Befehle sind „Automatisch an Inhalt anpassen“, „Automatisch an Fenster anpassen“ und „Feste Spaltenbreite“. In Microsoft Word legen diese Befehle relevante Tabelleneigenschaften fest und aktualisieren dann das Tabellenlayout und Aspose.Words erledigt das Gleiche für Sie.

### Beispiele

Zeigt, wie man eine neue Tabelle erstellt und dabei einen Stil anwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Wir müssen mindestens eine Zeile einfügen, bevor wir eine Tabellenformatierung festlegen.
builder.InsertCell();

// Legen Sie den verwendeten Tabellenstil basierend auf der Stilkennung fest.
// Beachten Sie, dass beim Speichern im .doc-Format nicht alle Tabellenstile verfügbar sind.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Den Stil basierend auf Prädikaten teilweise auf Features der Tabelle anwenden und dann die Tabelle erstellen.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Siehe auch

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


