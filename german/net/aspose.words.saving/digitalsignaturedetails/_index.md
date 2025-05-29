---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.DigitalSignatureDetails für nahtloses digitales Signieren von Dokumenten. Verbessern Sie mühelos Sicherheit und Authentizität!
type: docs
weight: 5640
url: /de/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

Enthält Details zum Signieren eines Dokuments mit einer digitalen Signatur.

```csharp
public class DigitalSignatureDetails
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | Initialisiert eine neue Instanz von`DigitalSignatureDetails` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | Ruft ab oder setzt einen[`CertificateHolder`](./certificateholder/) Objekt, das das zum Signieren eines Dokuments verwendete Zertifikat enthält. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | Ruft ab oder setzt einen[`SignOptions`](./signoptions/) Objekt zum Signieren eines Dokuments. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
