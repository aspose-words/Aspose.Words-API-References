---
title: PdfSaveOptions.DigitalSignatureDetails
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Çıktı PDF belgesini imzalamak için ayrıntıları alır veya ayarlar.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Çıktı PDF belgesini imzalamak için ayrıntıları alır veya ayarlar.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

### Notlar

Varsayılan değer boştur ve çıktı belgesi imzalanmayacaktır. Bu özellik geçerli bir değere ayarlandığında[`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) nesne, sonra çıktı PDF belgesi dijital olarak imzalanacaktır.

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

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


