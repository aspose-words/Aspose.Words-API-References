---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words für .NET
description: Entdecken Sie die Tabelleneigenschaft „AllowAutoFit“, um die Größe von Tabellenzellen in Microsoft Word und Aspose.Words mühelos anzupassen und so die Lesbarkeit und Präsentation Ihres Dokuments zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Ermöglicht Microsoft Word und Aspose.Words, die Größe von Zellen in einer Tabelle automatisch an ihren Inhalt anzupassen.

```csharp
public bool AllowAutoFit { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR`.

## Beispiele

Zeigt, wie die automatische Größenanpassung von Tabellenzellen aktiviert/deaktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Setzen Sie die Eigenschaft "AllowAutoFit" auf "false", damit die Tabelle die Abmessungen beibehält
// aller Zeilen und Zellen und kürzen Sie den Inhalt, wenn er zu groß wird, um hineinzupassen.
// Setzen Sie die Eigenschaft „AllowAutoFit“ auf „true“, damit die Tabelle die Breite und Höhe ihrer Zellen ändern kann
// um ihren Inhalt unterzubringen.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
