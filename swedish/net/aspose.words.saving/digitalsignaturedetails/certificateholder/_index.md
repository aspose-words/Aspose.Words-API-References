---
title: DigitalSignatureDetails.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words för .NET
description: Upptäck egenskapen DigitalSignatureDetails CertificateHolder för att enkelt hantera ditt dokuments signeringscertifikat. Förbättra säkerheten och effektivisera processer!
type: docs
weight: 20
url: /sv/net/aspose.words.saving/digitalsignaturedetails/certificateholder/
---
## DigitalSignatureDetails.CertificateHolder property

Hämtar eller ställer in en`CertificateHolder` objekt som innehåller certifikatet som används för att signera ett dokument.

```csharp
public CertificateHolder CertificateHolder { get; set; }
```

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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [DigitalSignatureDetails](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
