---
title: PdfEncryptionDetails.UserPassword
second_title: Referencia de API de Aspose.Words para .NET
description: PdfEncryptionDetails propiedad. Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado.
type: docs
weight: 40
url: /es/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado.

```csharp
public string UserPassword { get; set; }
```

### Observaciones

Se requerirá la contraseña de usuario para abrir un documento PDF cifrado para verlo. Los permisos especificados en [`Permissions`](../permissions/) será aplicado por el software del lector.

La contraseña de usuario puede ser`nulo` o cadena vacía, en este caso no se requerirá contraseña del usuario cuando abra el documento PDF. La contraseña de usuario no puede ser la misma que la contraseña del propietario.

### Ejemplos

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
* espacio de nombres [Aspose.Words.Saving](../../pdfencryptiondetails/)
* asamblea [Aspose.Words](../../../)


