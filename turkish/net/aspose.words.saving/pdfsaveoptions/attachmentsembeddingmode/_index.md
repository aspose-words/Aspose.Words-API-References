---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: .NET için Aspose.Words
description: PdfSaveOptions ile eklerin PDF'lere nasıl yerleştirileceğini özelleştirin. Sorunsuz entegrasyon ve optimize edilmiş belge paylaşımı sağlayın.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

Eklerin PDF belgesine nasıl yerleştirileceğini belirleyen bir değer alır veya ayarlar.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## Notlar

Varsayılan değerNone ve ekler yerleştirilmemiştir.

PDF/A-1, PDF/A-2 ve normal PDF/A-4 (PDF/A-4f değil) standartları gömülü dosyalara izin vermez. None değer otomatik olarak kullanılacaktır.

## Örnekler

PDF belgesine gömülü eklerin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
