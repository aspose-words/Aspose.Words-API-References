---
title: PdfEncryptionDetails.OwnerPassword
linktitle: OwnerPassword
articleTitle: OwnerPassword
second_title: Aspose.Words para .NET
description: PdfEncryptionDetails OwnerPassword propiedad. Especifica la contraseña del propietario del documento PDF cifrado en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Especifica la contraseña del propietario del documento PDF cifrado.

```csharp
public string OwnerPassword { get; set; }
```

## Observaciones

La contraseña del propietario permite al usuario abrir un documento PDF cifrado sin ninguna restricción de acceso especificada en[`Permissions`](../permissions/).

La contraseña del propietario no puede ser la misma que la contraseña del usuario.

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

* class [PdfEncryptionDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
