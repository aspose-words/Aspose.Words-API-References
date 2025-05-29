---
title: DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words för .NET
description: Upptäck konstruktorn DigitalSignatureDetails för att enkelt initiera digitala signaturinstanser, vilket förbättrar din applikations säkerhet och effektivitet.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails constructor

Initierar en ny instans av[`DigitalSignatureDetails`](../) klass.

```csharp
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| certificateHolder | CertificateHolder | En certifikatinnehavare som innehåller själva certifikatet. |
| signOptions | SignOptions | Signaturalternativ att använda för att signera ett dokument. |

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
* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
