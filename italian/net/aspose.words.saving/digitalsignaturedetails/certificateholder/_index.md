---
title: DigitalSignatureDetails.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words per .NET
description: Scopri la proprietà DigitalSignatureDetails CertificateHolder per gestire il certificato di firma dei tuoi documenti in modo semplice. Migliora la sicurezza e semplifica i processi!
type: docs
weight: 20
url: /it/net/aspose.words.saving/digitalsignaturedetails/certificateholder/
---
## DigitalSignatureDetails.CertificateHolder property

Ottiene o imposta un`CertificateHolder` oggetto che contiene il certificato utilizzato per firmare un documento.

```csharp
public CertificateHolder CertificateHolder { get; set; }
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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [DigitalSignatureDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
