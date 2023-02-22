---
title: PdfDigitalSignatureTimestampSettings.UserName
second_title: Aspose.Words for .NET API Referansı
description: PdfDigitalSignatureTimestampSettings mülk. Zaman damgası sunucusu kullanıcı adı.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/
---
## PdfDigitalSignatureTimestampSettings.UserName property

Zaman damgası sunucusu kullanıcı adı.

```csharp
public string UserName { get; set; }
```

### Notlar

Varsayılan değer null.

### Örnekler

Kaydedilmiş bir PDF belgesinin dijital olarak nasıl imzalanacağını ve ona zaman damgası vurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

 // Bir dijital imza oluşturun ve belgeyi PDF'ye kaydettiğimizde imzalamak için SaveOptions nesnemize atayın.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Yetkili tarafından doğrulanmış bir zaman damgası oluşturun.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// Zaman damgasının varsayılan ömrü 100 saniyedir.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Yapıcı aracılığıyla zaman aşımı süremizi ayarlayabiliriz.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// "Kaydet" yöntemi, şu anda çıktı belgesine imzamızı uygulayacaktır.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Ayrıca bakınız

* class [PdfDigitalSignatureTimestampSettings](../)
* ad alanı [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* toplantı [Aspose.Words](../../../)


