---
title: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words for .NET API Referansı
description: Bu sınıfın bir örneğini başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings() {#constructor}

Bu sınıfın bir örneğini başlatır.

```csharp
public PdfDigitalSignatureTimestampSettings()
```

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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings)
* ad alanı [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings)
* toplantı [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string) {#constructor_1}

Bu sınıfın bir örneğini başlatır.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| serverUrl | String | Zaman damgası sunucusu URL'si. |
| userName | String | Zaman damgası sunucusu kullanıcı adı. |
| password | String | Zaman damgası sunucu şifresi. |

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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings)
* ad alanı [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings)
* toplantı [Aspose.Words](../../../)

---

## PdfDigitalSignatureTimestampSettings(string, string, string, TimeSpan) {#constructor_2}

Bu sınıfın bir örneğini başlatır.

```csharp
public PdfDigitalSignatureTimestampSettings(string serverUrl, string userName, string password, 
    TimeSpan timeout)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| serverUrl | String | Zaman damgası sunucusu URL'si. |
| userName | String | Zaman damgası sunucusu kullanıcı adı. |
| password | String | Zaman damgası sunucu şifresi. |
| timeout | TimeSpan | Zaman damgası sunucusuna erişim için zaman aşımı değeri. |

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

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings)
* ad alanı [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
