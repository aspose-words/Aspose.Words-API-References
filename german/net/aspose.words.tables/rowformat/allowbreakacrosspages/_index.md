---
title: RowFormat.AllowBreakAcrossPages
second_title: Aspose.Words für .NET-API-Referenz
description: RowFormat eigendom. True wenn der Text in einer Tabellenzeile über einen Seitenumbruch geteilt werden darf.
type: docs
weight: 10
url: /de/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

True, wenn der Text in einer Tabellenzeile über einen Seitenumbruch geteilt werden darf.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### Beispiele

Zeigt, wie der seitenübergreifende Zeilenumbruch für jede Zeile in einer Tabelle deaktiviert wird.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Setzen Sie die Eigenschaft „AllowBreakAcrossPages“ auf „false“, um die Zeile beizubehalten
// in einem Stück, wenn eine Tabelle zwei Seiten umfasst, die entlang dieser Zeile aufgeteilt werden.
// Wenn die Zeile zu groß ist, um auf eine Seite zu passen, verschiebt Microsoft Word sie nach unten auf die nächste Seite.
// Setzen Sie die Eigenschaft „AllowBreakAcrossPages“ auf „true“, damit die Zeile auf zwei Seiten aufgeteilt werden kann.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Siehe auch

* class [RowFormat](../)
* namensraum [Aspose.Words.Tables](../../rowformat/)
* Montage [Aspose.Words](../../../)


