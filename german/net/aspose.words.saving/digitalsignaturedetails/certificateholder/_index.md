---
title: DigitalSignatureDetails.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „DigitalSignatureDetails CertificateHolder“, um das Signaturzertifikat Ihres Dokuments mühelos zu verwalten. Erhöhen Sie die Sicherheit und optimieren Sie Prozesse!
type: docs
weight: 20
url: /de/net/aspose.words.saving/digitalsignaturedetails/certificateholder/
---
## DigitalSignatureDetails.CertificateHolder property

Ruft ab oder setzt einen`CertificateHolder` Objekt, das das zum Signieren eines Dokuments verwendete Zertifikat enthält.

```csharp
public CertificateHolder CertificateHolder { get; set; }
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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [DigitalSignatureDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
