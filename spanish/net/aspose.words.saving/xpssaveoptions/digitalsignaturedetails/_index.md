---
title: XpsSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words para .NET
description: Descubra la propiedad XpsSaveOptions DigitalSignatureDetails para administrar fácilmente las firmas digitales para la firma segura de documentos y una autenticidad mejorada.
type: docs
weight: 20
url: /es/net/aspose.words.saving/xpssaveoptions/digitalsignaturedetails/
---
## XpsSaveOptions.DigitalSignatureDetails property

Obtiene o establece[`DigitalSignatureDetails`](../../digitalsignaturedetails/) objeto utilizado para firmar un documento.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Ejemplos

Muestra cómo firmar un documento XPS.

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

### Ver también

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
