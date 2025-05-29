---
title: PdfDigitalSignatureTimestampSettings Class
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: .NET için Aspose.Words
description: Kusursuz dijital imza zaman damgası yönetimi için Aspose.Words.PdfDigitalSignatureTimestampSettings'i keşfedin. PDF güvenliğinizi zahmetsizce artırın!
type: docs
weight: 6240
url: /tr/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class

Dijital imza zaman damgasının ayarlarını içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public class PdfDigitalSignatureTimestampSettings
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor)() | Bu sınıfın bir örneğini başlatır. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_1)(*string, string, string*) | Bu sınıfın bir örneğini başlatır. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_2)(*string, string, string, TimeSpan*) | Bu sınıfın bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Password](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/) { get; set; } | Zaman damgası sunucusu şifresi. |
| [ServerUrl](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/) { get; set; } | Zaman damgası sunucusu URL'si. |
| [Timeout](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/) { get; set; } | Zaman damgası sunucusuna erişim için zaman aşımı değeri. |
| [UserName](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/) { get; set; } | Zaman damgası sunucusu kullanıcı adı. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
