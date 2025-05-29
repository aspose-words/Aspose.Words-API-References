---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: .NET için Aspose.Words
description: MarkdownSaveOptions ExportAsHtml özelliğinin, HTML öğelerini sorunsuz Markdown dışa aktarımı için nasıl özelleştirmenize olanak sağladığını keşfedin. İçeriğinizin çok yönlülüğünü en üst düzeye çıkarın!
type: docs
weight: 30
url: /tr/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

Markdown'a ham HTML olarak aktarılacak öğelerin belirtilmesine olanak tanır. Varsayılan değerNone .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

## Örnekler

Bir tablonun ham HTML olarak Markdown'a nasıl aktarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Tablo oluştur.
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

### Ayrıca bakınız

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
