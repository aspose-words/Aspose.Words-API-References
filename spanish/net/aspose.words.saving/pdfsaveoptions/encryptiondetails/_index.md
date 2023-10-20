---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words para .NET
description: PdfSaveOptions EncryptionDetails propiedad. Obtiene o establece los detalles para cifrar el documento PDF de salida en C#.
type: docs
weight: 130
url: /es/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Obtiene o establece los detalles para cifrar el documento PDF de salida.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Observaciones

El valor predeterminado es`nulo` y el documento de salida no se cifrará. Cuando esta propiedad se establece en un valor válido[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, entonces el documento PDF de salida se cifrará.

El algoritmo de cifrado AES-128 se utiliza al guardar en formato PDF 1.7 (incluido PDF/UA-1). El algoritmo de cifrado AES-256 se utiliza al guardar en formato PDF 2.0.

El cifrado está prohibido por el cumplimiento de PDF/A. Esta opción se ignorará al guardar en PDF/A.

ContentCopyForAccessibility Se requiere permiso para cumplimiento de PDF/UA si el documento de salida está cifrado. Este permiso se utilizará automáticamente al guardar en PDF/UA.

ContentCopyForAccessibility El permiso está obsoleto en formato PDF 2.0. Este permiso se ignorará al guardar en PDF 2.0.

## Ejemplos

Muestra cómo establecer permisos en un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Ampliar permisos para permitir la edición de anotaciones.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Habilite el cifrado mediante la propiedad "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// Cuando abramos este documento, necesitaremos proporcionar la contraseña antes de acceder a su contenido.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ver también

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
