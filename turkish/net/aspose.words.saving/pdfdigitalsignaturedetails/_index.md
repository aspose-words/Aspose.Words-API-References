---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfDigitalSignatureDetails sınıf. PDF belgesini dijital imzayla imzalamaya ilişkin ayrıntıları içerir C#'da.
type: docs
weight: 5430
url: /tr/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

PDF belgesini dijital imzayla imzalamaya ilişkin ayrıntıları içerir.

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
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Karma algoritmayı alır veya ayarlar. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | İmzalamanın konumunu alır veya ayarlar. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | İmzalama nedenini alır veya ayarlar. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | İmzalama tarihini alır veya ayarlar. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Dijital imza zaman damgası ayarlarını alır veya ayarlar. |

## Notlar

Şu anda PDF belgelerini dijital olarak imzalamak yalnızca .NET 2.0 veya üzeri sürümlerde mümkündür.

Aspose.Words tarafından oluşturulan bir PDF belgesini dijital olarak imzalamak için,[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) özelliğini geçerli bir`PdfDigitalSignatureDetails` nesneyi seçin ve ardından belgeyi ileterek PDF formatında kaydedin.[`PdfSaveOptions`](../pdfsaveoptions/) parametre olarak[`Save`](../../aspose.words/document/save/) yöntem.

Aspose.Words, tüm PDF belgesi üzerinde bir PKCS#7 imzası oluşturur ve dijital imza oluştururken "Adobe.PPKMS" filtresini ve "adbe.pkcs7.sha1" alt filtresini kullanır.

## Örnekler

Oluşturulan bir PDF belgesinin nasıl imzalanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "SaveOptions" nesnesinin "DigitalSignatureDetails" nesnesini yapılandırın
// belgeyi "Kaydet" yöntemiyle oluştururken dijital olarak imzalayın.
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
