---
title: XpsSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words für .NET
description: Entdecken Sie die DigitalSignatureDetails-Eigenschaft von XpsSaveOptions zur einfachen Verwaltung digitaler Signaturen für sicheres Signieren von Dokumenten und verbesserte Authentizität.
type: docs
weight: 20
url: /de/net/aspose.words.saving/xpssaveoptions/digitalsignaturedetails/
---
## XpsSaveOptions.DigitalSignatureDetails property

Ruft ab oder legt fest[`DigitalSignatureDetails`](../../digitalsignaturedetails/) Objekt zum Signieren eines Dokuments.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Beispiele

Zeigt, wie ein XPS-Dokument signiert wird.

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

### Siehe auch

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [XpsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
