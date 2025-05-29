---
title: Table.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Table StyleIdentifier“, um lokal unabhängige Tabellenstile einfach zu verwalten und so Ihre Datenpräsentation mühelos zu verbessern.
type: docs
weight: 280
url: /de/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Ruft die gebietsschemaunabhängige Stilkennung des auf diese Tabelle angewendeten Tabellenstils ab oder legt diese fest.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Beispiele

Zeigt, wie beim Anwenden eines Stils eine neue Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Wir müssen mindestens eine Zeile einfügen, bevor wir eine Tabellenformatierung festlegen.
builder.InsertCell();

// Legen Sie den verwendeten Tabellenstil basierend auf der Stilkennung fest.
// Beachten Sie, dass beim Speichern im DOC-Format nicht alle Tabellenstile verfügbar sind.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Wenden Sie den Stil teilweise auf Funktionen der Tabelle basierend auf Prädikaten an und erstellen Sie dann die Tabelle.
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

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
