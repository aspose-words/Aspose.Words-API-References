---
title: PdfSaveOptions.DigitalSignatureDetails
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Obtiene o establece los detalles para firmar el documento PDF de salida.
type: docs
weight: 60
url: /es/net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Obtiene o establece los detalles para firmar el documento PDF de salida.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

### Observaciones

El valor predeterminado es nulo y el documento de salida no se firmará. Cuando esta propiedad se establece en un valor válido[`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) object, , el documento PDF de salida se firmará digitalmente.

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

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


