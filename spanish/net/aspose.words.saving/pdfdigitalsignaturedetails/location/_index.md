---
title: PdfDigitalSignatureDetails.Location
second_title: Referencia de API de Aspose.Words para .NET
description: PdfDigitalSignatureDetails propiedad. Obtiene o establece la ubicación de la firma.
type: docs
weight: 40
url: /es/net/aspose.words.saving/pdfdigitalsignaturedetails/location/
---
## PdfDigitalSignatureDetails.Location property

Obtiene o establece la ubicación de la firma.

```csharp
public string Location { get; set; }
```

### Observaciones

El valor por defecto es nulo.

### Ejemplos

Muestra cómo firmar un documento PDF generado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configure el objeto "DigitalSignatureDetails" del objeto "SaveOptions" para
// firma digitalmente el documento a medida que lo renderizamos con el método "Guardar".
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Ver también

* class [PdfDigitalSignatureDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* asamblea [Aspose.Words](../../../)


