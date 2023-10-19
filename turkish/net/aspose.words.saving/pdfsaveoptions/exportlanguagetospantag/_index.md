---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words for .NET
description: PdfSaveOptions ExportLanguageToSpanTag mülk. Metin dilini dışa aktarmak için belge yapısında bir Span etiketi oluşturulup oluşturulmayacağını belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Metin dilini dışa aktarmak için belge yapısında bir "Span" etiketi oluşturulup oluşturulmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`ve "Lang" özelliği, bir sayfa içerik akışındaki işaretli içerik dizisine eklenir.

Değer ne zaman`doğru` Varsayılan olmayan language değerine sahip metin için "Span" etiketi oluşturulur ve bu etikete "Lang" özelliği eklenir.

Bu değer şu durumlarda göz ardı edilir:[`ExportDocumentStructure`](../exportdocumentstructure/) dır-dir`YANLIŞ` .

## Örnekler

Metin dilini dışa aktarmak için belge yapısında bir "Span" etiketinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // "ExportDocumentStructure" yanlış olduğunda "ExportLanguageToSpanTag" seçeneğinin dikkate alınmadığını unutmayın.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
