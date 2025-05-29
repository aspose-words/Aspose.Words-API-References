---
title: PdfDigitalSignatureDetails.HashAlgorithm
linktitle: HashAlgorithm
articleTitle: HashAlgorithm
second_title: Aspose.Words para .NET
description: Descubra la propiedad HashAlgorithm de PdfDigitalSignatureDetails: administre y personalice de manera eficiente sus algoritmos hash para una mayor seguridad digital.
type: docs
weight: 30
url: /es/net/aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/
---
## PdfDigitalSignatureDetails.HashAlgorithm property

Obtiene o establece el algoritmo hash.

```csharp
public PdfDigitalSignatureHashAlgorithm HashAlgorithm { get; set; }
```

## Observaciones

El valor predeterminado es el algoritmo SHA-256.

## Ejemplos

Muestra cómo firmar un documento PDF generado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configure el objeto "DigitalSignatureDetails" del objeto "SaveOptions" para
// Firmamos digitalmente el documento a medida que lo renderizamos con el método "Guardar".
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Ver también

* enum [PdfDigitalSignatureHashAlgorithm](../../pdfdigitalsignaturehashalgorithm/)
* class [PdfDigitalSignatureDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
