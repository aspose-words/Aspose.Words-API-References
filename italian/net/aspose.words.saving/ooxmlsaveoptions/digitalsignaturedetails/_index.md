---
title: OoxmlSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words per .NET
description: Esplora la proprietà DigitalSignatureDetails di OoxmlSaveOptions per gestire in modo efficiente le firme digitali per una firma sicura dei documenti e una maggiore conformità.
type: docs
weight: 40
url: /it/net/aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/
---
## OoxmlSaveOptions.DigitalSignatureDetails property

Ottiene o imposta[`DigitalSignatureDetails`](../../digitalsignaturedetails/) oggetto utilizzato per firmare un documento.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Esempi

Mostra come firmare un documento OOXML.

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

### Guarda anche

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
