---
title: DocumentBuilder.Writeln
linktitle: Writeln
articleTitle: Writeln
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti senza sforzo con il metodo Writeln di DocumentBuilder inserisci testo e interruzioni di paragrafo senza problemi per una migliore leggibilità.
type: docs
weight: 700
url: /it/net/aspose.words/documentbuilder/writeln/
---
## Writeln(*string*) {#writeln_1}

Inserisce una stringa e un'interruzione di paragrafo nel documento.

```csharp
public void Writeln(string text)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| text | String | Stringa da inserire nel documento. |

## Osservazioni

Formato del carattere e del paragrafo corrente specificato da[`Font`](../font/) E[`ParagraphFormat`](../paragraphformat/) vengono utilizzate le proprietà.

## Esempi

Mostra come creare una tabella formattata 2x2.

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

// Durante la creazione della tabella, il generatore di documenti applicherà i valori correnti delle proprietà RowFormat/CellFormat
// alla riga/cella corrente in cui si trova il cursore e a tutte le nuove righe/celle man mano che vengono create.
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

// Le righe e le celle aggiunte in precedenza non vengono retroattivamente influenzate dalle modifiche apportate alla formattazione del builder.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Writeln() {#writeln}

Inserisce un'interruzione di paragrafo nel documento.

```csharp
public void Writeln()
```

## Osservazioni

chiamate[`InsertParagraph`](../insertparagraph/).

## Esempi

Mostra come creare intestazioni e piè di pagina in un documento utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specificare che si vogliono intestazioni e piè di pagina diversi per la prima pagina, le pagine pari e quelle dispari.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crea le intestazioni, quindi aggiungi tre pagine al documento per visualizzare ciascun tipo di intestazione.
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

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
