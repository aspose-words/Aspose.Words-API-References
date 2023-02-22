---
title: PdfDigitalSignatureDetails.PdfDigitalSignatureDetails
second_title: Referencia de API de Aspose.Words para .NET
description: PdfDigitalSignatureDetails constructor. Inicializa una instancia de esta clase.
type: docs
weight: 10
url: /es/net/aspose.words.saving/pdfdigitalsignaturedetails/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails() {#constructor}

Inicializa una instancia de esta clase.

```csharp
public PdfDigitalSignatureDetails()
```

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

---

## PdfDigitalSignatureDetails(CertificateHolder, string, string, DateTime) {#constructor_1}

Inicializa una instancia de esta clase.

```csharp
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, string reason, 
    string location, DateTime signatureDate)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| certificateHolder | CertificateHolder | Un titular de certificado que contiene el propio certificado. |
| reason | String | El motivo de la firma. |
| location | String | El lugar de la firma. |
| signatureDate | DateTime | La fecha y hora de la firma. |

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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [PdfDigitalSignatureDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* asamblea [Aspose.Words](../../../)


