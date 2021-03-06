---
title: EncryptionDetails
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece los detalles para cifrar el documento PDF de salida.
type: docs
weight: 110
url: /es/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Obtiene o establece los detalles para cifrar el documento PDF de salida.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

### Observaciones

El valor predeterminado es nulo y el documento de salida no se cifrará. Cuando esta propiedad se establece en un valor válido[`PdfEncryptionDetails`](../../pdfencryptiondetails) object, entonces el documento PDF de salida se cifrará.

El algoritmo de cifrado AES-128 se usa cuando se guarda en cumplimiento basado en PDF 1.7 (incluido PDF/UA-1). El algoritmo de cifrado AES-256 se usa cuando se guarda en cumplimiento basado en PDF 2.0.

El cifrado está prohibido por el cumplimiento de PDF/A. Esta opción se ignorará al guardar en PDF/A.

ContentCopyForAccessibilityel permiso es requerido por el cumplimiento de PDF/UA si el documento de salida está encriptado. Este permiso se utilizará automáticamente al guardar en PDF/UA.

ContentCopyForAccessibility el permiso está obsoleto en el formato PDF 2.0. Este permiso se ignorará al guardar en PDF 2.0.

### Ejemplos

Muestra cómo establecer permisos en un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Comience por desautorizar todos los permisos.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Ampliar permisos para permitir la edición de anotaciones.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Habilite el cifrado a través de la propiedad "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// Cuando abramos este documento, necesitaremos proporcionar la contraseña antes de acceder a su contenido.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ver también

* class [PdfEncryptionDetails](../../pdfencryptiondetails)
* class [PdfSaveOptions](../../pdfsaveoptions)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
