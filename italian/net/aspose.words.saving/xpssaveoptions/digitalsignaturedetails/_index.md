---
title: XpsSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words per .NET
description: Scopri la proprietà DigitalSignatureDetails di XpsSaveOptions per gestire facilmente le firme digitali per una firma sicura dei documenti e una maggiore autenticità.
type: docs
weight: 20
url: /it/net/aspose.words.saving/xpssaveoptions/digitalsignaturedetails/
---
## XpsSaveOptions.DigitalSignatureDetails property

Ottiene o imposta[`DigitalSignatureDetails`](../../digitalsignaturedetails/) oggetto utilizzato per firmare un documento.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Esempi

Mostra come firmare un documento XPS.

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions options = new SignOptions();
options.SignTime = DateTime.Now;
options.Comments = "Some comments";

DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(certificateHolder, options);

XpsSaveOptions saveOptions = new XpsSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "XpsSaveOptions.XpsDigitalSignature.docx", saveOptions);
```

### Guarda anche

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [XpsSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
