---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.DigitalSignatureDetails para una firma digital de documentos fluida. ¡Mejore la seguridad y la autenticidad sin esfuerzo!
type: docs
weight: 5640
url: /es/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

Contiene detalles para firmar un documento con una firma digital.

```csharp
public class DigitalSignatureDetails
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | Inicializa una nueva instancia de`DigitalSignatureDetails` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | Obtiene o establece un[`CertificateHolder`](./certificateholder/) objeto que contiene el certificado utilizado para firmar un documento. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | Obtiene o establece un[`SignOptions`](./signoptions/) objeto utilizado para firmar un documento. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
