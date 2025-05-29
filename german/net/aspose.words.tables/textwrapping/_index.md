---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Tables.TextWrapping für effizienten Textumbruch um Tabellen. Verbessern Sie mühelos die Formatierung Ihrer Dokumente!
type: docs
weight: 7230
url: /de/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

Gibt an, wie der Text um die Tabelle herum umbrochen wird.

```csharp
public enum TextWrapping
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Text und Tabelle werden in der Reihenfolge ihres Auftretens im Dokument angezeigt. |
| Around | `1` | Der Text wird um die Tabelle herumgeführt und belegt den verfügbaren seitlichen Platz. |
| Default | `0` | Standardwert. |

## Beispiele

Zeigt, wie mit dem Textumbruch in Tabellen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Setzen Sie die Eigenschaft „TextWrapping“ auf „TextWrapping.Around“, damit die Tabelle den Text umschließt.
// und schieben Sie es durch Festlegen der Position in den darunter liegenden Absatz.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)
