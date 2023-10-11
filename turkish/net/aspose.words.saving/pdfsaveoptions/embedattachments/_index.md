---
title: PdfSaveOptions.EmbedAttachments
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Eklerin PDF belgesine gömülüp gömülmeyeceğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 110
url: /tr/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Eklerin PDF belgesine gömülüp gömülmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool EmbedAttachments { get; set; }
```

### Notlar

Varsayılan değer:`YANLIŞ`ve ekler gömülü değildir.

Değer ne zaman`doğru` ekler PDF belgesine gömülür.

PDF/A ve PDF/UA uyumluluğuna kaydederken eklerin gömülmesi desteklenmez. `YANLIŞ` değer otomatik olarak kullanılacaktır.

Şifreleme etkinleştirildiğinde eklerin eklenmesi desteklenmez.`YANLIŞ` value otomatik olarak kullanılacaktır.

### Örnekler

PDF belgesine gömme eklerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


