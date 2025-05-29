---
title: DigitalSignatureDetails.SignOptions
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SignOptions di DigitalSignatureDetails migliora la sicurezza dei documenti gestendo facilmente le opzioni di firma per firme digitali senza interruzioni.
type: docs
weight: 30
url: /it/net/aspose.words.saving/digitalsignaturedetails/signoptions/
---
## DigitalSignatureDetails.SignOptions property

Ottiene o imposta un`SignOptions` oggetto utilizzato per firmare un documento.

```csharp
public SignOptions SignOptions { get; set; }
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

* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
