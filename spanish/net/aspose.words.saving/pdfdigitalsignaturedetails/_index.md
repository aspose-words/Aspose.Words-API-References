---
title: Class PdfDigitalSignatureDetails
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.PdfDigitalSignatureDetails clase. Contiene detalles para firmar un documento PDF con una firma digital.
type: docs
weight: 5150
url: /es/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Contiene detalles para firmar un documento PDF con una firma digital.

```csharp
public class PdfDigitalSignatureDetails
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Inicializa una instancia de esta clase. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(CertificateHolder, string, string, DateTime) | Inicializa una instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Devuelve el objeto del titular del certificado que contiene el certificado que se utilizó para firmar el documento. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Obtiene o establece el algoritmo hash. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Obtiene o establece la ubicación de la firma. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Obtiene o establece el motivo de la firma. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Obtiene o establece la fecha de la firma. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Obtiene o establece la configuración de la marca de tiempo de la firma digital. |

### Observaciones

Por el momento, la firma digital de documentos PDF solo está disponible en .NET 2.0 o superior.

Para firmar digitalmente un documento PDF cuando lo crea Aspose.Words, configure el[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) propiedad a una válida`PdfDigitalSignatureDetails` objeto y luego guarde el documento en formato PDF pasando el[`PdfSaveOptions`](../pdfsaveoptions/)como parámetro en el[`Save`](../../aspose.words/document/save/) método.

Aspose.Words crea una firma PKCS#7 sobre todo el documento PDF y utiliza el filtro "Adobe.PPKMS" y el subfiltro "adbe.pkcs7.sha1" al crear una firma digital.

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


