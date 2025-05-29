---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: .NET için Aspose.Words
description: PDF belgelerinizin kalite ve uyumluluk açısından endüstri standartlarını karşıladığından emin olmak için PdfSaveOptions Uyumluluk özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Çıktı belgeleri için PDF standartlarına uyumluluk düzeyini belirtir.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Notlar

VarsayılanPdf17.

## Örnekler

Kaydedilen PDF belgelerinin PDF standartlarına uygunluk düzeyinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
// Standartlardan birine kaydederken bazı PdfSaveOptions'ların yasaklandığını ve otomatik olarak düzeltildiğini unutmayın.
// Hangi seçeneklerin otomatik olarak düzeltildiğini bilmek için IWarningCallback'i kullanın.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "PDF/A-1b" standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfA1b" olarak ayarlayın,
// Aspose.Words'ün PDF'e dönüştürmesiyle belgenin görsel görünümünün korunması amaçlanır.
// "1.7" standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.Pdf17" olarak ayarlayın.
// "PDF/A-1a" standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfA1a" olarak ayarlayın,
// "PDF/A-1b" ile uyumlu olup, orijinal belgenin belge yapısını da korumaktadır.
// "PDF/UA-1" (ISO 14289-1) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfUa1" olarak ayarlayın,
// PDF formatında elektronik dokümanların erişilebilir olmasını sağlayan tanımlamaları amaçlamaktadır.
// "PDF 2.0" (ISO 32000-2) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.Pdf20" olarak ayarlayın.
// "PDF/A-4" (ISO 19004:2020) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfA4" olarak ayarlayın,
// zaman içerisinde belgenin statik görsel görünümünü koruyan.
// Hem PDF/A-4 (ISO 19005-4:2020) hem de PDF/A-4 (ISO 19005-4:2020) ile uyumlu olması için "Uyumluluk" özelliğini "PdfCompliance.PdfA4Ua2" olarak ayarlayın
// ve PDF/UA-2 (ISO 14289-2:2024) standartları.
// PDF/UA-2 (ISO 14289-2:2024) standardına uymak için "Uyumluluk" özelliğini "PdfCompliance.PdfUa2" olarak ayarlayın.
// Bu, belgelerin aranabilir olmasına yardımcı olur ancak zaten büyük olan belgelerin boyutunu önemli ölçüde artırabilir.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
