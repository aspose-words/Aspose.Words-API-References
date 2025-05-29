---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportAsHtml di MarkdownSaveOptions ti permette di personalizzare gli elementi HTML per un'esportazione Markdown fluida. Massimizza la versatilità dei tuoi contenuti!
type: docs
weight: 30
url: /it/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

Consente di specificare gli elementi da esportare in Markdown come HTML grezzo. Il valore predefinito èNone .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

## Esempi

Mostra come esportare una tabella in Markdown come HTML grezzo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Crea tabella.
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### Guarda anche

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
