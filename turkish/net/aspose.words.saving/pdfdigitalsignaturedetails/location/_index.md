---
title: PdfDigitalSignatureDetails.Location
linktitle: Location
articleTitle: Location
second_title: .NET için Aspose.Words
description: Gelişmiş güvenlik ve verimlilik için belge imzalama konumunuzu kolayca yönetmek ve özelleştirmek amacıyla PdfDigitalSignatureDetails Location özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/pdfdigitalsignaturedetails/location/
---
## PdfDigitalSignatureDetails.Location property

İmzalamanın konumunu alır veya ayarlar.

```csharp
public string Location { get; set; }
```

## Notlar

Varsayılan değer:`hükümsüz` .

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

* class [PdfDigitalSignatureDetails](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
