---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: .NET için Aspose.Words
description: Sorunsuz PDF dijital imzalama için Aspose.Words.PdfDigitalSignatureDetails sınıfını keşfedin. Kolay entegrasyon ve sağlam özellikler ile belge güvenliğini artırın.
type: docs
weight: 6220
url: /tr/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Bir PDF belgesini dijital imzayla imzalamaya ilişkin ayrıntıları içerir.

```csharp
public class PdfDigitalSignatureDetails
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Bu sınıfın bir örneğini başlatır. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | Bu sınıfın bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Karma algoritmasını alır veya ayarlar. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | İmzalamanın konumunu alır veya ayarlar. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | İmzalamanın nedenini alır veya ayarlar. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | İmzalamanın tarihini alır veya ayarlar. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Dijital imza zaman damgası ayarlarını alır veya ayarlar. |

## Notlar

Şu anda PDF belgelerini dijital olarak imzalamak yalnızca .NET 3.5 ve üzeri sürümlerde mümkündür.

Aspose.Words tarafından oluşturulduğunda bir PDF belgesini dijital olarak imzalamak için,[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) özelliğini geçerli bir özelliğe dönüştürün`PdfDigitalSignatureDetails` nesneyi ve ardından belgeyi ile PDF formatında kaydedin[`PdfSaveOptions`](../pdfsaveoptions/) bir parametre olarak[`Save`](../../aspose.words/document/save/) yöntem.

Aspose.Words, tüm PDF belgesi üzerinde bir PKCS#7 imzası oluşturur ve dijital imza oluştururken "Adobe.PPKMS" filtresini ve "adbe.pkcs7.sha1" alt filtresini kullanır.

## Örnekler

Oluşturulan bir PDF belgesinin nasıl imzalanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "SaveOptions" nesnesinin "DigitalSignatureDetails" nesnesini yapılandırın
// "Kaydet" metoduyla oluşturduğumuz belgeyi dijital olarak imzalıyoruz.
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
