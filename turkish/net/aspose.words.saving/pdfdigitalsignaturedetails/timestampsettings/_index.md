---
title: PdfDigitalSignatureDetails.TimestampSettings
linktitle: TimestampSettings
articleTitle: TimestampSettings
second_title: .NET için Aspose.Words
description: Gelişmiş belge güvenliği ve uyumluluğu için dijital imza zaman damgalarını kolayca yönetmek üzere PdfDigitalSignatureDetails TimestampSettings özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/
---
## PdfDigitalSignatureDetails.TimestampSettings property

Dijital imza zaman damgası ayarlarını alır veya ayarlar.

```csharp
public PdfDigitalSignatureTimestampSettings TimestampSettings { get; set; }
```

## Notlar

Varsayılan değer:`hükümsüz` ve dijital imza zaman damgalı olmayacaktır. Bu özellik geçerli bir değere ayarlandığında[`PdfDigitalSignatureTimestampSettings`](../../pdfdigitalsignaturetimestampsettings/) nesne, ise PDF belgesindeki dijital imza zaman damgalı olacaktır.

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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/)
* class [PdfDigitalSignatureDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
