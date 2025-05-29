---
title: DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words per .NET
description: Scopri il costruttore DigitalSignatureDetails per inizializzare facilmente le istanze di firma digitale, migliorando la sicurezza e l'efficienza della tua applicazione.
type: docs
weight: 10
url: /it/net/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails constructor

Inizializza una nuova istanza di[`DigitalSignatureDetails`](../) classe.

```csharp
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certificateHolder | CertificateHolder | Un titolare di certificato che contiene il certificato stesso. |
| signOptions | SignOptions | Opzioni di firma da utilizzare per firmare un documento. |

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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
