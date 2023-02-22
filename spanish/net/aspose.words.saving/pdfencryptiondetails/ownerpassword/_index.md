---
title: PdfEncryptionDetails.OwnerPassword
second_title: Referencia de API de Aspose.Words para .NET
description: PdfEncryptionDetails propiedad. Especifica la contraseña de propietario para el documento PDF encriptado.
type: docs
weight: 20
url: /es/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Especifica la contraseña de propietario para el documento PDF encriptado.

```csharp
public string OwnerPassword { get; set; }
```

### Observaciones

La contraseña de propietario permite al usuario abrir un documento PDF encriptado sin ninguna restricción de acceso especificada en[`Permissions`](../permissions/).

La contraseña de propietario no puede ser la misma que la contraseña de usuario.

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

* class [PdfEncryptionDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfencryptiondetails/)
* asamblea [Aspose.Words](../../../)


