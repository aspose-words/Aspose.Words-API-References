---
title: PdfDigitalSignatureDetails.Reason
second_title: Aspose.Words for .NET API Referansı
description: PdfDigitalSignatureDetails mülk. İmzalama nedenini alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/pdfdigitalsignaturedetails/reason/
---
## PdfDigitalSignatureDetails.Reason property

İmzalama nedenini alır veya ayarlar.

```csharp
public string Reason { get; set; }
```

### Notlar

Varsayılan değer null.

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

* class [PdfDigitalSignatureDetails](../)
* ad alanı [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* toplantı [Aspose.Words](../../../)


