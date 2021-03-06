---
title: PdfDigitalSignatureHashAlgorithm
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica un algoritmo hash digital utilizado por una firma digital.
type: docs
weight: 5160
url: /es/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Especifica un algoritmo hash digital utilizado por una firma digital.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Sha256 | `0` | Algoritmo hash SHA-256. |
| Sha384 | `1` | Algoritmo hash SHA-384. |
| Sha512 | `2` | Algoritmo hash SHA-512. |
| RipeMD160 | `3` | Algoritmo hash RIPEMD-160. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
