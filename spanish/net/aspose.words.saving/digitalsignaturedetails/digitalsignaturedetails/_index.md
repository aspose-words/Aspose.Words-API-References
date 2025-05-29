---
title: DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words para .NET
description: Descubra el constructor DigitalSignatureDetails para inicializar fácilmente instancias de firma digital, mejorando la seguridad y la eficiencia de su aplicación.
type: docs
weight: 10
url: /es/net/aspose.words.saving/digitalsignaturedetails/digitalsignaturedetails/
---
## DigitalSignatureDetails constructor

Inicializa una nueva instancia de[`DigitalSignatureDetails`](../) clase.

```csharp
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| certificateHolder | CertificateHolder | Un titular de certificado que contiene el certificado en sí. |
| signOptions | SignOptions | Opciones de firma para utilizar al firmar un documento. |

## Ejemplos

Muestra cómo firmar un documento OOXML.

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

### Ver también

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [SignOptions](../../../aspose.words.digitalsignatures/signoptions/)
* class [DigitalSignatureDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
