---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad UserPassword mejora la seguridad de PDF al requerir una contraseña para acceder, garantizando así que sus documentos permanezcan protegidos y confidenciales.
type: docs
weight: 40
url: /es/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Especifica la contraseña de usuario necesaria para abrir el documento PDF cifrado.

```csharp
public string UserPassword { get; set; }
```

## Observaciones

Se requerirá la contraseña del usuario para abrir un documento PDF cifrado y visualizarlo. Los permisos especificados en [`Permissions`](../permissions/) será aplicado por el software del lector.

La contraseña del usuario puede ser`nulo` o cadena vacía; en este caso, no se solicitará contraseña al usuario al abrir el documento PDF. La contraseña del usuario no puede ser la misma que la del propietario.

## Ejemplos

Muestra cómo establecer permisos en un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

//Ampliar los permisos para permitir la edición de anotaciones.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Habilite el cifrado a través de la propiedad "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

//Cuando abramos este documento, necesitaremos proporcionar la contraseña antes de acceder a su contenido.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ver también

* class [PdfEncryptionDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
