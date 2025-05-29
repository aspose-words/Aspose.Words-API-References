---
title: MarkdownSaveOptions.TableContentAlignment
linktitle: TableContentAlignment
articleTitle: TableContentAlignment
second_title: Aspose.Words per .NET
description: Scopri la proprietà TableContentAlignment di MarkdownSaveOptions per personalizzare l'allineamento del contenuto della tabella per esportazioni Markdown fluide. L'impostazione predefinita è Auto.
type: docs
weight: 140
url: /it/net/aspose.words.saving/markdownsaveoptions/tablecontentalignment/
---
## MarkdownSaveOptions.TableContentAlignment property

Ottiene o imposta un valore che specifica come allineare i contenuti nelle tabelle durante l'esportazione inMarkdown format. Il valore predefinito èAuto .

```csharp
public TableContentAlignment TableContentAlignment { get; set; }
```

## Esempi

Mostra come allineare i contenuti nelle tabelle.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { TableContentAlignment = tableContentAlignment };

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

Document doc = new Document(ArtifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
Table table = doc.FirstSection.Body.Tables[0];

switch (tableContentAlignment)
{
    case TableContentAlignment.Auto:
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Left:
        Assert.AreEqual(ParagraphAlignment.Left,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Left,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Center:
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Right:
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
}
```

### Guarda anche

* enum [TableContentAlignment](../../tablecontentalignment/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
