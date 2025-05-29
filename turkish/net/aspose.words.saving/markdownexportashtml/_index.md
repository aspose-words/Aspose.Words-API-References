---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: .NET için Aspose.Words
description: Markdown öğelerini ham HTML'ye zahmetsizce dönüştürmek ve belge dışa aktarma seçeneklerinizi geliştirmek için Aspose.Words.Saving.MarkdownExportAsHtml enum'ını keşfedin.
type: docs
weight: 6020
url: /tr/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Markdown'a ham HTML olarak aktarılacak öğelerin belirtilmesine olanak tanır.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Herhangi bir ham HTML kullanmadan Markdown sözdizimini kullanarak tüm öğeleri dışa aktarın. |
| Tables | `1` | Tabloları ham HTML olarak dışa aktar. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
