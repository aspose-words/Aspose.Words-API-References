---
title: DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words für .NET
description: Entdecken Sie den DigitalSignatureDetails-Konstruktor, um digitale Signaturinstanzen einfach zu initialisieren und so die Sicherheit und Effizienz Ihrer Anwendung zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails constructor

Initialisiert eine neue Instanz von[`DigitalSignatureDetails`](../) Klasse.

```csharp
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certificateHolder | CertificateHolder | Ein Zertifikatshalter, der das Zertifikat selbst enthält. |
| signOptions | SignOptions | Signaturoptionen zum Signieren eines Dokuments. |

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
* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
