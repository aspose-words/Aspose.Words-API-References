---
title: PdfDigitalSignatureTimestampSettings.ServerUrl
linktitle: ServerUrl
articleTitle: ServerUrl
second_title: .NET için Aspose.Words
description: Güvenli zaman damgası için PdfDigitalSignatureTimestampSettings ServerUrl özelliğini keşfedin. Güvenilir zaman damgası sunucusu URL'leriyle belge bütünlüğünü sağlayın.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/
---
## PdfDigitalSignatureTimestampSettings.ServerUrl property

Zaman damgası sunucusu URL'si.

```csharp
public string ServerUrl { get; set; }
```

## Notlar

Varsayılan değer:`hükümsüz` . Eğer`hükümsüz` , o zaman dijital imza zaman damgalı olmayacaktır.

## Örnekler

Kaydedilmiş bir PDF belgesinin dijital olarak nasıl imzalanacağını ve zaman damgasının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Dijital bir imza oluşturup bunu SaveOptions nesnemize atayarak belgeyi PDF'e kaydettiğimizde imzalayalım.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Zaman damgası yetkisi doğrulanmış bir zaman damgası oluşturun.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Zaman damgasının varsayılan ömrü 100 saniyedir.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Zaman aşımı süresini constructor üzerinden ayarlayabiliriz.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", seçenekler.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// "Kaydet" metodu imzamızı bu aşamada çıktı belgesine uygulayacaktır.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Ayrıca bakınız

* class [PdfDigitalSignatureTimestampSettings](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
