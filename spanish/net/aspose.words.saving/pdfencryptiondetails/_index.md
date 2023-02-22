---
title: Class PdfEncryptionDetails
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.PdfEncryptionDetails clase. Contiene detalles para el cifrado y permisos de acceso para un documento PDF.
type: docs
weight: 5180
url: /es/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Contiene detalles para el cifrado y permisos de acceso para un documento PDF.

```csharp
public class PdfEncryptionDetails
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/)(string, string) | Inicializa una instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Especifica la contraseña de propietario para el documento PDF encriptado. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. El valor predeterminado esDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Especifica la contraseña de usuario necesaria para abrir el documento PDF cifrado. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


