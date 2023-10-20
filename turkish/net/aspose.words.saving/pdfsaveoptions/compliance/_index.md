---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: PdfSaveOptions Compliance mülk. Çıktı belgeleri için PDF standartları uyumluluk düzeyini belirtir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Çıktı belgeleri için PDF standartları uyumluluk düzeyini belirtir.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Notlar

Varsayılan:Pdf17.

## Örnekler

Kaydedilen PDF belgelerinin PDF standartlarına uygunluk düzeyinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
// Standartlardan birine kaydederken bazı PdfSaveOptions'ın yasak olduğunu ve otomatik olarak düzeltildiğini unutmayın.
// Hangi seçeneklerin otomatik olarak düzeltildiğini öğrenmek için IWarningCallback'i kullanın.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "PDF/A-1b" standardına uyum sağlamak için "Compliance" özelliğini "PdfCompliance.PdfA1b" olarak ayarlayın,
// Aspose.Words onu PDF'ye dönüştürürken belgenin görsel görünümünü korumayı amaçlar.
// "1.7" standardına uyum sağlamak için "Compliance" özelliğini "PdfCompliance.Pdf17" olarak ayarlayın.
// "PDF/A-1a" standardına uyum sağlamak için "Compliance" özelliğini "PdfCompliance.PdfA1a" olarak ayarlayın,
// "PDF/A-1b" ile uyumlu ve aynı zamanda orijinal belgenin belge yapısını koruyan.
// "PDF/UA-1" (ISO 14289-1) standardına uyum sağlamak için "Compliance" özelliğini "PdfCompliance.PdfUa1" olarak ayarlayın,
// dosyanın erişilebilir olmasını sağlayan PDF'deki elektronik belgeleri temsil etmeyi tanımlamayı amaçlamaktadır.
// "PDF 2.0" (ISO 32000-2) standardına uyum sağlamak için "Compliance" özelliğini "PdfCompliance.Pdf20" olarak ayarlayın.
// "PDF/A-4" (ISO 19004:2020) standardına uyum sağlamak için "Compliance" özelliğini "PdfCompliance.PdfA4" olarak ayarlayın,
// belgenin statik görsel görünümünü zaman içinde koruyan.
// Bu, belgelerin aranabilir olmasına yardımcı olur ancak zaten büyük olan belgelerin boyutunu önemli ölçüde artırabilir.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
