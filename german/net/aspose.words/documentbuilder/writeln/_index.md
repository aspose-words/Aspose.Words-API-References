---
title: DocumentBuilder.Writeln
linktitle: Writeln
articleTitle: Writeln
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der Writeln-Methode von DocumentBuilder – fügen Sie nahtlos Text- und Absatzumbrüche ein, um die Lesbarkeit zu verbessern.
type: docs
weight: 700
url: /de/net/aspose.words/documentbuilder/writeln/
---
## Writeln(*string*) {#writeln_1}

Fügt eine Zeichenfolge und einen Absatzumbruch in das Dokument ein.

```csharp
public void Writeln(string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Die in das Dokument einzufügende Zeichenfolge. |

## Bemerkungen

Aktuelle Schriftart und Absatzformatierung, angegeben durch[`Font`](../font/) Und[`ParagraphFormat`](../paragraphformat/) Eigenschaften werden verwendet.

## Beispiele

Zeigt, wie eine formatierte 2x2-Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Beim Erstellen der Tabelle wendet der Dokumentgenerator seine aktuellen RowFormat/CellFormat-Eigenschaftswerte an
// zur aktuellen Zeile/Zelle, in der sich der Cursor befindet, und zu allen neuen Zeilen/Zellen, sobald diese erstellt werden.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Zuvor hinzugefügte Zeilen und Zellen werden durch Änderungen an der Formatierung des Builders nicht rückwirkend beeinflusst.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Writeln() {#writeln}

Fügt einen Absatzumbruch in das Dokument ein.

```csharp
public void Writeln()
```

## Bemerkungen

Anrufe[`InsertParagraph`](../insertparagraph/).

## Beispiele

Zeigt, wie Sie mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir für die erste, die gerade und die ungerade Seite unterschiedliche Kopf- und Fußzeilen wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dem Dokument dann drei Seiten hinzu, um jeden Kopfzeilentyp anzuzeigen.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
