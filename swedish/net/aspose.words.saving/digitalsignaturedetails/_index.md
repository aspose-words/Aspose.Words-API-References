---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.DigitalSignatureDetails för sömlös digital dokumentsignering. Förbättra säkerhet och autenticitet utan ansträngning!
type: docs
weight: 5640
url: /sv/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

Innehåller information om hur man signerar ett dokument med en digital signatur.

```csharp
public class DigitalSignatureDetails
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | Initierar en ny instans av`DigitalSignatureDetails` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | Hämtar eller ställer in en[`CertificateHolder`](./certificateholder/) objekt som innehåller certifikatet som används för att signera ett dokument. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | Hämtar eller ställer in en[`SignOptions`](./signoptions/) objekt som används för att signera ett dokument. |

## Exempel

Visar hur man signerar OOXML-dokument.

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(
    certificateHolder,
    new SignOptions() { Comments = "Some comments", SignTime = DateTime.Now });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
