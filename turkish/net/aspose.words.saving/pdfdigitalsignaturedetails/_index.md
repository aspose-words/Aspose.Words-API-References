---
title: Class PdfDigitalSignatureDetails
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfDigitalSignatureDetails sınıf. Dijital imzalı bir PDF belgesini imzalamaya ilişkin ayrıntıları içerir.
type: docs
weight: 5150
url: /tr/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Dijital imzalı bir PDF belgesini imzalamaya ilişkin ayrıntıları içerir.

```csharp
public class PdfDigitalSignatureDetails
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Bu sınıfın bir örneğini başlatır. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(CertificateHolder, string, string, DateTime) | Bu sınıfın bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Karma algoritmasını alır veya ayarlar. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | İmzalamanın konumunu alır veya ayarlar. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | İmzalama nedenini alır veya ayarlar. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | İmzalama tarihini alır veya ayarlar. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Dijital imza zaman damgası ayarlarını alır veya ayarlar. |

### Notlar

Şu anda PDF belgelerini dijital olarak imzalamak yalnızca .NET 2.0 veya üzeri sürümlerde mevcuttur.

Aspose.Words tarafından oluşturulduğunda bir PDF belgesini dijital olarak imzalamak için,[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) özelliği geçerli bir`PdfDigitalSignatureDetails` nesneyi seçin ve ardından belgeyi geçen PDF formatında kaydedin.[`PdfSaveOptions`](../pdfsaveoptions/)parametre olarak[`Save`](../../aspose.words/document/save/) yöntem.

Aspose.Words, tüm PDF belgesi üzerinde bir PKCS#7 imzası oluşturur ve dijital imza oluştururken "Adobe.PPKMS" filtresini ve "adbe.pkcs7.sha1" alt filtresini kullanır.

### Örnekler

Oluşturulan bir PDF belgesinin nasıl imzalanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "SaveOptions" nesnesinin "DigitalSignatureDetails" nesnesini şu şekilde yapılandırın:
// "Kaydet" yöntemiyle belgeyi oluşturduğumuz gibi dijital olarak imzalıyoruz.
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


