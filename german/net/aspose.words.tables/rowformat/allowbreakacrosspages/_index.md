---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words für .NET
description: Entdecken Sie die RowFormat-Eigenschaft AllowBreakAcrossPages, die einen nahtlosen Textfluss in Tabellenzeilen über Seitenumbrüche hinweg ermöglicht, um die Lesbarkeit und Darstellung zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Wahr, wenn der Text in einer Tabellenzeile über einen Seitenumbruch hinweg aufgeteilt werden darf.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Beispiele

Zeigt, wie Sie den Zeilenumbruch über mehrere Seiten hinweg für jede Zeile einer Tabelle deaktivieren.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Setzen Sie die Eigenschaft "AllowBreakAcrossPages" auf "false", um die Zeile beizubehalten
// in einem Stück, wenn sich eine Tabelle über zwei Seiten erstreckt, die entlang dieser Zeile unterbrochen werden.
// Wenn die Zeile zu groß ist, um auf eine Seite zu passen, verschiebt Microsoft Word sie auf die nächste Seite.
// Setzen Sie die Eigenschaft „AllowBreakAcrossPages“ auf „true“, um die Aufteilung der Zeile auf zwei Seiten zuzulassen.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Siehe auch

* class [RowFormat](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
