---
title: PdfSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: .NET için Aspose.Words
description: PDF imzalama ayrıntılarını kolayca yönetmek, güvenli ve etkili belge çıktısı sağlamak için PdfSaveOptions DigitalSignatureDetails'ı keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Çıktı PDF belgesinin imzalanması için ayrıntıları alır veya ayarlar.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Notlar

Varsayılan değer:`hükümsüz` ve çıktı belgesi imzalanmayacaktır. Bu özellik geçerli bir değere ayarlandığında[`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) nesne, ise çıktı PDF belgesi dijital olarak imzalanacaktır.

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

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
