---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfDigitalSignatureHashAlgorithm Sıralama. Dijital imza tarafından kullanılan dijital karma algoritmayı belirtir C#'da.
type: docs
weight: 5440
url: /tr/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Dijital imza tarafından kullanılan dijital karma algoritmayı belirtir.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Sha256 | `0` | SHA-256 karma algoritması. |
| Sha384 | `1` | SHA-384 karma algoritması. |
| Sha512 | `2` | SHA-512 karma algoritması. |
| RipeMD160 | `3` | RIPEMD-160 karma algoritması. |

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
