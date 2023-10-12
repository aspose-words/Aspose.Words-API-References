---
title: PdfEncryptionDetails.Permissions
second_title: Referencia de API de Aspose.Words para .NET
description: PdfEncryptionDetails propiedad. Especifica las operaciones permitidas a un usuario en un documento PDF cifrado. El valor predeterminado esDisallowAll .
type: docs
weight: 30
url: /es/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Especifica las operaciones permitidas a un usuario en un documento PDF cifrado. El valor predeterminado esDisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfencryptiondetails/)
* asamblea [Aspose.Words](../../../)


