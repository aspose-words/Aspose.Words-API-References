---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words para .NET
description: Explore la enumeración Aspose.Words PdfDigitalSignatureHashAlgorithm, que define algoritmos hash digitales para firmas digitales seguras en sus documentos.
type: docs
weight: 6230
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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
