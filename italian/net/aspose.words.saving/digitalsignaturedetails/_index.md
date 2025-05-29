---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.DigitalSignatureDetails per una firma digitale impeccabile dei documenti. Migliora sicurezza e autenticità senza sforzo!
type: docs
weight: 5640
url: /it/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

Contiene i dettagli per firmare un documento con una firma digitale.

```csharp
public class DigitalSignatureDetails
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | Inizializza una nuova istanza di`DigitalSignatureDetails` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | Ottiene o imposta un[`CertificateHolder`](./certificateholder/) oggetto che contiene il certificato utilizzato per firmare un documento. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | Ottiene o imposta un[`SignOptions`](./signoptions/) oggetto utilizzato per firmare un documento. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
