---
title: OoxmlSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words för .NET
description: Utforska OoxmlSaveOptions egenskap DigitalSignatureDetails för att effektivt hantera digitala signaturer för säker dokumentsignering och förbättrad efterlevnad.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/
---
## OoxmlSaveOptions.DigitalSignatureDetails property

Hämtar eller sätter[`DigitalSignatureDetails`](../../digitalsignaturedetails/) objekt som används för att signera ett dokument.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
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

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
