---
title: Class PdfEncryptionDetails
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.PdfEncryptionDetails clase. Contiene detalles para cifrar y permisos de acceso a un documento PDF.
type: docs
weight: 5460
url: /es/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Contiene detalles para cifrar y permisos de acceso a un documento PDF.

Para obtener más información, visite el[Proteger o cifrar un documento](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) artículo de documentación.

```csharp
public class PdfEncryptionDetails
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(string, string) | Inicializa una instancia de esta clase. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(string, string, PdfPermissions) | Inicializa una instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Especifica la contraseña del propietario del documento PDF cifrado. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Especifica las operaciones permitidas a un usuario en un documento PDF cifrado. El valor predeterminado esDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


