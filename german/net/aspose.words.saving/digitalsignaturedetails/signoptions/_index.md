---
title: DigitalSignatureDetails.SignOptions
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SignOptions-Eigenschaft von DigitalSignatureDetails die Dokumentsicherheit verbessert, indem sie Signaturoptionen für nahtlose digitale Signaturen einfach verwaltet.
type: docs
weight: 30
url: /de/net/aspose.words.saving/digitalsignaturedetails/signoptions/
---
## DigitalSignatureDetails.SignOptions property

Ruft ab oder setzt einen`SignOptions` Objekt zum Signieren eines Dokuments.

```csharp
public SignOptions SignOptions { get; set; }
```

## Beispiele

Zeigt, wie ein OOXML-Dokument signiert wird.

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

### Siehe auch

* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
